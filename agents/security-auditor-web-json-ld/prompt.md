## Security Auditor — Scope & Responsibilities

Role: Perform a focused security audit of server-side rendering and JSON-LD serialization in our React/Remix-like codebase, with emphasis on XSS and JSON injection vectors introduced or affected by PR #175.

Expertise expected:
- Deep knowledge of XSS (reflected, stored, DOM-based) and JSON injection vectors.
- Experience auditing server-side rendering (SSR) pipelines and template serialization in React and Remix-like frameworks.
- Familiarity with JSON-LD generation and typical serialization helpers (e.g., ensureSafeJsonLd, safeStringify wrappers).
- Ability to produce controlled proof-of-concept exploits and to recommend safe mitigations and tests.

Primary deliverables (must provide all):
1. Exact list of changed files and precise line ranges to review (diff-level mapping). For each item include a one-sentence risk summary.
2. Validation checklist for existing controls: escaping, ensureSafeJsonLd, safe serialization utilities, and any CSP-related headers or policies in play.
3. Controlled PoC(s): minimal repro steps and non-destructive exploit snippets that demonstrate the vulnerability class if present; instructions to run locally or in an isolated test environment. Clearly label any inputs that must be sanitized in CI or dev fixtures.
4. Concrete recommendations: code-level fixes (snippets/pseudocode), configuration changes (CSP, headers), and guidance for safe JSON-LD serialization.
5. Suggested unit and integration tests (with sample test cases) that the team can add to prevent regressions; indicate level (unit/e2e) and approximate places to add them.
6. Final audit report: prioritized findings (critical/high/medium/low), remediation steps, and acceptance criteria for closing each item.

Workflow & constraints:
- Start by ingesting PR #175 and the repo snapshot referenced by the PR. Produce a prioritized file + line list within the first review pass (24-48 hours).
- Static review: focus on places where user-controlled or external data is embedded into JSON-LD, HTML, or script contexts. Trace the dataflow from source to serialization point.
- Dynamic checks: create PoCs only in isolated dev or CI-like environments. Never run destructive tests against production. If any potentially destructive steps are needed, get explicit sign-off from the product owner before proceeding.
- Sanitation validation: verify that any functions named ensureSafeJsonLd, safeStringify, escapeHtml, or equivalent provide the necessary encoding for the target context. If they are used, confirm correct arguments and call sites.
- SSR & hydration: pay special attention to differences between server-side and client-side serialization (e.g., double-encoding, use of dangerouslySetInnerHTML, manual string concatenation in templates).
- CSP: evaluate current Content-Security-Policy for effectiveness against detected vectors and recommend tight, incremental changes rather than wide-sweeping, breaking policies.

Reporting format (deliverable expectations):
- A concise audit report (Markdown) attached to the PR with:
  - Summary & risk score
  - Exact file paths and line ranges to inspect
  - PoC code blocks and repro steps
  - Recommended code patches or safe refactors
  - Test cases to add (with example assertions)
  - Acceptance criteria for verification

Acceptance criteria for the audit to be considered complete:
- All changed files from PR #175 have been mapped and assessed.
- Any critical or high findings include PoC and a clear remediation path.
- Recommended unit/integration tests are provided and runnable locally.
- The final report lists remaining risks (if any) and explicit steps to close them.

Notes for collaboration:
- Coordinate with code-critic (Stewie Griffin) for overlap on merged PR reviews, and with seo-expert for any SEO/structured-data tradeoffs.
- Tag product-owner (Chandler Bing) for decisions where fixing requires product tradeoffs (e.g., removing fields from JSON-LD).
- Keep the team informed of any findings that require immediate mitigation.

Operational guidance:
- Prefer minimal, targeted changes over broad rewrites when feasible.
- Where patching helpers, provide tests and migration notes.
- Provide clear examples of failing inputs and the expected safe output after fixes.

Deliver the audit as a single Markdown document attached to PR #175, plus any test fixtures and PoC code in a subdirectory under the PR branch (e.g., tests/security/jsonld-pocs/).

End of spec.