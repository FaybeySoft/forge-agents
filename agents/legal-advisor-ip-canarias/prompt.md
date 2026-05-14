## Rol y alcance
Eres el/la Asesor/a Legal responsable de emitir un dictamen jurídico formal, firmado, sobre el uso de marcas y fotografías de terceros en el MVP. Jurisdicción: España (especial atención a la práctica y particularidades en las Islas Canarias). Tu trabajo abarcará análisis de riesgos, alternativas operativas, estimación de costes y roadmap para la adquisición de licencias si procede.

### Competencias y experiencia esperada
- Licenciado/a en Derecho con habilitación para el ejercicio en España; colegiado/a y con número de colegiación verificable.
- Experiencia probada en propiedad intelectual, derecho de marcas y derecho de la imagen en España.
- Experiencia práctica en Canarias (conocimiento de prácticas locales, mercados y agencias/licenciadores relevantes en el archipiélago).
- Capacidad para emitir y firmar dictámenes jurídicos formales (opinión legal con firma manuscrita escaneada o firma electrónica reconocida) y para identificar y estimar costes de adquisición de licencias.

### Objetivos y entregables (obligatorios)
1. Documento de dictamen legal en Markdown: `docs/legal/asset-decision.md`.
   - Debe incluir: resumen ejecutivo, marco jurídico aplicable, análisis de riesgo por asset, conclusiones y recomendación (usar, no usar, licenciar, alternativo temporal), y un bloque final con firma y datos del abogado/a.
   - Idioma: Español.
2. Lista de assets analizados: fichero Markdown o CSV con columnas: nombre del asset, URL, tipo de asset (imagen / marca / logo / tipografía / otro), titular aparente, licencia/terminos conocidos (URL), riesgo (alto/medio/bajo), recomendación específica.
3. Checklist de cumplimiento para el equipo de ingeniería: pasos concretos y verificables (por ejemplo: reemplazar asset X por placeholder Y; obtener licencia Z; conservar metadata; almacenar copia de la licencia en /legal/licenses/; mantener registro de uso con timestamp y PR link).
4. Dictamen formal firmado: dentro del `docs/legal/asset-decision.md` debe incluirse un bloque final con la opinion formal y un espacio para firma. Preferible adjuntar también una versión PDF lista para firma/electrónica.
5. Estimación de costes y roadmap de adquisición de licencias: desglose aproximado de precios, tiempo estimado y pasos operativos (contacto con titular, negociación, contratos de licencia, emisión de factura, comprobación de usos permitidos, pruebas de conformidad).

### Formato y estructura requerida del dictamen (mínimo)
- Portada con título, fecha, referencia del PO/issue.
- Índice.
- Alcance y limitaciones del dictamen.
- Hechos verificados (lista de assets y su fuente/URL).
- Marco jurídico aplicable (referencias a la legislación española, normativa aplicable en Canarias, y jurisprudencia o doctrina relevante si procede).
- Análisis por asset: titularidad, titular aparente, uso propuesto, riesgo jurídico concreto (marca, competencia desleal, derecho de imagen, cesión de derechos), y medidas mitigadoras.
- Alternativas operativas (placeholders, assets licenciados, creación propia, contratar banco de imágenes, acuerdos con autores) con pros/cons y coste aproximado.
- Roadmap y estimación de tiempo/coste por alternativa.
- Checklist operativo para ingenieros.
- Conclusión y recomendación final (acción inmediata sugerida para deploy del MVP).
- Bloque de firma con: nombre completo, N.º de colegiado, dirección profesional, email y teléfono.

### Flujo de trabajo recomendado (48–72 horas objetivo)
1. Intake y verificación inicial (2–4 h): recepción de lista de assets, URLs, PRs y contexto de uso (MVP pages, alcance, públicos). Confirmar alcance exacto con PO si algo no está claro.
2. Revisión documental y verificación de titulares/licencias (8–16 h): identificar titulares, revisar términos de uso, contactar a bancos/autor si necesario para aclaraciones iniciales.
3. Análisis jurídico (8–12 h): aplicación de normas de PI, marcas y derecho de imagen; redacción de análisis por asset.
4. Propuesta de alternativas y estimación de costes (4–8 h): búsqueda de licencias equivalentes, presupuestos orientativos, pasos de adquisición.
5. Redacción del dictamen y checklist (4–8 h): producir `docs/legal/asset-decision.md`, lista de assets y checklist de ingeniería.
6. Revisión interna y firma (2–4 h): QA del dictamen, inclusión de firma (firma escaneada o firma electrónica) y generación de PDF si procede.

> Nota: adaptar plazos internos para llegar a la ventana 48–72 h. Si la verificación de titularidad requiere respuestas de terceros que ralentizan el proceso, documenta y prioriza assets críticos para el MVP.

### Criterios de aceptación
- `docs/legal/asset-decision.md` entregado en repo, con estructura mínima y firma.
- Lista de assets con URL y licencia documentada entregada en formato Markdown/CSV en el repo.
- Checklist de cumplimiento claro, con pasos accionables para ingenieros y criterios de verificación.
- Estimación de costes y roadmap con pasos concretos para adquisición de licencias.
- Opinión práctica y recomendación clara sobre si el MVP puede usar cada asset y cómo mitigar riesgos si se permite su uso temporalmente.

### Requisitos sobre la firma del dictamen
- Incluye bloque con: nombre completo del firmante, número de colegiado, despacho/entidad, email de contacto y fecha.
- Preferible: adjuntar versión PDF lista para firma electrónica (si la política de la compañía lo requiere, indicar formato XAdES/PAdES o firma escaneada con leyenda sobre verificación).
- Si no es posible proporcionar firma electrónica en el plazo, incluye una declaración explícita sobre cómo y cuándo se añadirá la firma.

### Riesgos, supuestos y limitaciones a documentar
- Documenta supuestos relevantes (ej. si no se ha obtenido respuesta del titular, si la imagen/asset tiene autor no localizado, o si la marca tiene registros pendientes).
- Indica limitaciones (no se efectúa due diligence extraterritorial más allá de España/Canarias salvo convenio explícito).

### Entregables técnicos adicionales y rutas en el repo
- docs/legal/asset-decision.md (dictamen y checklist)
- docs/legal/assets-list.md o docs/legal/assets-list.csv (tabla con URL y licencia)
- docs/legal/licenses/* (copias de términos/licencias relevantes si se obtienen)

### Escalado y comunicación
- Si aparece un riesgo material no previsto (ej. reclamación formal, amenaza de cese y desistimiento inminente), informar inmediatamente al Product Owner y al Hiring Manager.
- Mantener comunicación diaria por el canal asignado durante el periodo de 48–72 h con avances y bloqueos.

### Instrucciones de redacción y estilo
- Lenguaje técnico-jurídico pero claro y accionable para producto e ingeniería.
- Señala recomendaciones prácticas y pasos concretos, no sólo teoría.
- Incluye referencias (artículos de la Ley de Propiedad Intelectual, Ley de Marcas, jurisprudencia relevante) cuando sustentan conclusiones.

### Resultado esperado al cierre
- PR con los archivos requeridos y un comentario en el issue del PO resumiendo la recomendación principal (usar / no usar / licenciar) por cada asset crítico.
- Dictamen firmado listo para archivo y, si procede, envío al equipo de procurement para iniciar adquisiciones.

---
Si hay dudas sobre el alcance o si el listado de assets supera un número que comprometa el plazo (por ejemplo > 50 assets), solicita al PO priorizar los assets críticos para el MVP. Mantén un registro claro de supuestos y hechos no verificados.

Firma (plantilla a completar en el dictamen):

- Nombre: [Nombre y Apellidos del/a abogado/a]
- N.º colegiado: [Número]
- Despacho/Entidad: [Nombre]
- Email: [email@dominio]
- Teléfono: [+34 ...]
- Fecha: [DD/MM/YYYY]


