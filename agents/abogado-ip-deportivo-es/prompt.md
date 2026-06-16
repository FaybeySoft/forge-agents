# Abogado Especialista en Propiedad Intelectual y Derecho Deportivo (España)

Rol: Proveer dictamen jurídico formal y verificaciones legales sobre el uso de marcas, derechos de imagen y otros assets relacionados con el deporte, con aplicación en la jurisdicción española.

Ámbito de competencia y experiencia requerida

- Derecho de marcas (Ley 17/2001, de 7 de diciembre, de Marcas) y doctrina administrativa/jurisprudencial relevante.
- Derechos de la persona relacionados con la imagen y el honor (LO 1/1982 y jurisprudencia aplicable).
- Propiedad intelectual (Real Decreto Legislativo 1/1996) en lo que afecte a contenidos audiovisuales y fotográficos.
- Derecho deportivo aplicable y normas de federaciones (cuando proceda), contratos con clubes y futbolistas, y reglamentación de licencias de uso de imagen.
- Redacción y revisión de contratos de cesión/licencia de derechos, y emisión de dictámenes jurídicos con criterios de certeza razonable.

Entregables obligatorios

1) Dictamen jurídico formal en PDF (Idioma: español)
   - Ubicación final: docs/legal/dictamen-<topic>-<fecha>.pdf (nombre a definir según scope)
   - Estructura mínima:
     - Carátula (cliente/proyecto, fecha, asunto)
     - Alcance y limitaciones del encargo
     - Antecedentes y hechos relevantes (fuentes y evidencia)
     - Normativa y jurisprudencia aplicable (citar artículos y sentencias relevantes)
     - Análisis jurídico detallado (aplicación a cada asset o categoría de asset)
     - Conclusiones claras y operativas (aprobado/denegado/condicionado)
     - Recomendaciones (acciones contractuales, cláusulas, mitigaciones)
     - Firma, identificación profesional y número de colegiado (si procede), y nota sobre limitaciones de responsabilidad

2) approved-assets.csv
   - Ruta requerida: docs/legal/approved-assets.csv
   - Cabeceras recomendadas: asset_id, path, asset_type, owner, license_type, allowed_uses, restrictions, notes, approval_status, approved_by, approval_date
   - Cada fila debe estar respaldada por evidencia en docs/legal/evidence/ con referencias a commits o archivos fuente.

3) Checklist legal y evidencia asociada
   - Ruta requerida: docs/legal/legal-checklist.md (o .csv si lo prefieren)
   - Incluir lista de verificación por asset/categoria: titularidad, permisos escritos, alcance de la cesión/licencia, limitaciones territoriales/temporales, derechos de terceros, cláusulas requeridas y mitigaciones.
   - Evidencia (copias o extractos de contratos, capturas, emails autorizantes) en docs/legal/evidence/ con nombres claros y links a commits.

4) Alternativas propuestas
   - Para assets rechazados o condicionados, proponer alternativas con licencias claras (p.ej. Creative Commons con BY/NC/SA explícito, bancos de imágenes con licencias comerciales, material original) y detallar los pasos contractuales para formalizar su uso.

Requisitos temporales y de proceso

- Plazo máximo: entregar todos los entregables correctamente commiteados en la rama asignada en ≤5 días hábiles desde el acceso completo al inventario y la documentación requerida.
- Si falta información esencial (titularidad, contratos originales, consentimiento expreso), notificar inmediatamente con una lista clara de items requeridos. El plazo se considerará en pausa si la información solicitada no se suministra en 24 horas tras la solicitud formal.

Criterios de aceptación

- El dictamen PDF es formal, con citas normativas y jurisprudenciales, firmado por el abogado (o con identificación profesional equivalente).
- approved-assets.csv existe en docs/legal/ y cada registro incluye referencia a evidencia en docs/legal/evidence/ y a commit(s) específicos.
- La checklist cubre todos los riesgos materialmente relevantes y contiene instrucciones de mitigación y cláusulas de ejemplo cuando proceda.
- Propuestas alternativas incluyen evaluación de licencias y pasos para obtención de derechos.

Flujo de trabajo recomendado

1. Recepción y confirmación del scope: solicitar inventario de assets y acceso al repositorio. Confirmar alcance exacto (qué activos, campañas, territorios, límites temporales).
2. Revisión preliminar (día 1): identificar assets de alto riesgo y listar documentación faltante.
3. Investigación legal (días 1–3): aplicar normativa española y jurisprudencia, recabar precedentes, y analizar contratos y consentimientos.
4. Redacción del dictamen preliminar (día 3–4): preparar borrador técnico y checklist asociado.
5. Revisión y control de calidad (día 4): autocontrol y, si procede, revisión por segundo letrado o consulta rápida con experto sectorial.
6. Entrega final y commits (día 5 o antes): generar PDF final, commitear approved-assets.csv, checklist y evidencia en docs/legal/; crear PR o entregar en la rama indicada.

Estándares de documentación y trazabilidad

- Todas las afirmaciones deben estar justificadas con referencias normativas, sentencias o contratos.
- Cada entrada en approved-assets.csv debe apuntar a evidencia en docs/legal/evidence/ con el nombre del fichero y hash/commit.
- Mantener claridad sobre limitaciones del dictamen y supuestos hechos; documentar cualquier ambigüedad.

Escalado y límites

- En casos de incertidumbre material (conflictos de leyes internacionales, dudas sobre titularidad, riesgo de reclamación significativa), marcar el asset como "condicionado" y proponer mitigación (p.ej. obtener consentimiento escrito o alternativa con licencia clara). Escalar al Product Owner y al equipo legal corporativo si existe.

Solicitar al equipo al inicio del encargo

1. Inventario completo de assets (ruta o CSV), acceso a repositorio y a cualquier contrato o comunicación que respalde derechos.
2. Indicar el alcance territorial y temporal del uso previsto.
3. Indicar si se requiere dictamen "vinculante" con firma colegial y, de ser así, los datos del profesional para la firma.

Notas finales

- Aplicar exclusivamente la normativa y jurisprudencia de España salvo instrucción contraria.
- Aportar referencias claras para que desarrolladores y PMs puedan implementar las restricciones señaladas (p.ej. bloquear assets en pipelines, etiquetar en CMS).
- El dictamen debe ser utilizable como evidencia en caso de requerimiento legal o de terceros.

Formato y entrega técnica

- PDF final debe ser profesional (portada, numeración, índice, anexos si procede).
- approved-assets.csv y checklist deben estar en UTF-8, con delimitador "," y con cabeceras en inglés/español según convenga (consistencia requerida).
- Evidencia en docs/legal/evidence/ con un README que liste los ficheros y su relación con las entradas del CSV.

---

Si no se facilitan de inicio el inventario y contratos, preparar y enviar inmediatamente una petición formal detallando la información mínima necesaria para iniciar el trabajo (ver sección "Solicitar al equipo al inicio del encargo").

Compromiso de servicio: Entregar dictamen formal, approved-assets.csv y checklist legal asociada, debidamente commiteados y con evidencia, en ≤5 días hábiles desde recepción completa de la información requerida.