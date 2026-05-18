## Asesor Legal — Propiedad Intelectual, Marcas y Licencias de Imágenes (web/html)

Objetivo

Proveer un dictamen legal inicial (no vinculante) en un plazo de 48 horas sobre el uso de assets gráficos en el MVP de estadísticas, incluyendo alcance permitido de uso de marcas y logos, lista de assets con riesgo de infracción, alternativas y licencias aceptables, y texto recomendado de atribución/licencias para incluir en el repo/PR. Además, preparar un checklist accionable para documentación in-repo en: `docs/legal/palmares-assets-decision.md`.

Alcance

- Análisis de assets gráficos incluidos en el repositorio o listados por el equipo (imágenes raster/vector, logos, ilustraciones, fotos con personas reconocibles, iconografía de terceros).  
- Evaluación de: titularidad, derechos de autor, marcas registradas, derechos de imagen/personalidad, licencias existentes, y uso permitido en contexto web/html (MVP).  
- Propuesta de alternativas (placeholders, ilustraciones libres, stock con licencia compatible) y texto legal a incluir en PR y en el repo.

Entregables (48h)

1. Dictamen legal inicial (formato Markdown):  
   - Resumen ejecutivo (1 párrafo).  
   - Para cada asset: estado (ALLOW / BLOCK / REVIEW-NEEDS), justificación legal breve y riesgo estimado.  
   - Alcance permitido de uso para marcas/logos detectados (ej. uso nominativo, uso decorativo, tamaño/contexto).  
   - Lista de assets con riesgo de infracción priorizados por criticidad.  
   - Alternativas y fuentes/licencias recomendadas (ej. licencias Creative Commons específicas, bancos de imágenes con términos comerciales, creación de ilustraciones propias).  
   - Texto recomendado para atribución/licencia para incluir en el repo y en el PR.  
2. Archivo checklist accionable (ruta propuesta): `docs/legal/palmares-assets-decision.md` — formato breve con pasos y responsabilidades.  
3. Texto sugerido para PR (copy listo para pegar) que explique la decisión legal y las acciones requeridas para merge.  

Flujo de trabajo y pasos requeridos

1. Recibir inputs del equipo:  
   - Lista de assets con rutas en el repo y URLs externas (si aplica).  
   - Metadatos disponibles (autor, origen, licencia, compras/recibos).  
   - Uso previsto (p. ej. icono UI, imagen de producto, marketing).  
   - Fecha límite de 48h y punto de contacto.  
2. Clasificación rápida (primeras 6 horas): identificar assets claramente libres o claramente con licencia problemática.  
3. Análisis detallado (hasta 36 horas): investigación de titularidad, búsqueda de marcas registradas relevantes, comprobación de licencias, y estimación de riesgo.  
4. Redacción del dictamen y checklist (últimas 6 horas).  
5. Entrega de los tres entregables y sesión breve (15-30 min) de Q&A con PO/UX/Dev si se requiere aclaración.

Criterios para decisión por asset

- ALLOW: evidencia clara de licencia/comercial usage permitida o uso legítimo (p. ej. assets creados por el equipo o con licencia explícita para uso comercial).  
- BLOCK: riesgo sustancial de infracción (marca registrada utilizada de manera que confunda, imagen sin licencia con persona reconocible, falta de permiso de titular).  
- REVIEW-NEEDS: ambigüedad en titularidad/uso que requiere más documentación o consulta con counsel externo.  

Formato y convenciones de salida

- Dictamen en Markdown (encabezados claros por asset).  
- Cada asset: nombre/ruta, estado (ALLOW/BLOCK/REVIEW-NEEDS), riesgo (alto/medio/bajo), acciones recomendadas (ej. reemplazar por X, adquirir licencia Y, obtener consentimiento).  
- Texto de atribución/licencia: proveer snippets listos para README y para footer de páginas si aplica.  
- PR copy: 1-3 párrafos explicativos + checklist bullets requeridos antes de merge.

Plantilla sugerida (ejemplo de fragmento para repo/PR)

- README / docs/legal/palmares-assets-decision.md:  
  - Fecha del dictamen: YYYY-MM-DD  
  - Autor: Asesor Legal (nombre)  
  - Resumen ejecutivo  
  - Tabla resumida por asset (ruta — estado — acción requerida)  

- Texto sugerido para PR:  
  "Se adjunta dictamen legal inicial sobre los assets incluidos en este PR. Actuar conforme a las recomendaciones listadas: (1) reemplazar assets BLOCK, (2) adjuntar licencia o comprobante para assets REVIEW-NEEDS antes de merge, (3) incluir las atribuciones sugeridas en el README. Véase docs/legal/palmares-assets-decision.md para detalle."  

Criterios de escalado a counsel externo

- Si un asset implicara riesgo elevado de reclamación por uso de marca o derecho de imagen de persona conocida y el impacto potencial en el producto es significativo.  
- Si la decisión pudiera requerir negociación de licencias/suplantación de marcas con terceros.  

Limitaciones

- Este dictamen es un análisis legal inicial y orientativo preparado con la información disponible. No sustituye un dictamen vinculante de asesoría legal externa con representación.

Comunicación y entregables finales

- Entregar:  
  - `dictamen-palmares-assets-YYYYMMDD.md`  
  - `docs/legal/palmares-assets-decision.md` (checklist)  
  - `pr-text-palmares-assets-YYYYMMDD.md` (texto sugerido para PR)  
- Entregar en español.  
- Incluir referencias (URL a registros de marcas, páginas de licencias, capturas de pantalla si es relevante).

Criterios de aceptación por el PO

- Dictamen entregado en 48 horas con: lista por asset y estado, alternativas/licitaciones propuestas, texto listo para repo/PR y checklist in-repo.
- Claridad suficiente para que UX + FA + devs puedan aplicar las recomendaciones sin exponer el proyecto a reclamaciones inmediatas.

Si no hay información suficiente sobre un asset, marcar como REVIEW-NEEDS y detallar qué evidencia se requiere (ej. comprobante de compra, licencia, permiso escrito del titular).

---

Notas finales

- Mantener trazabilidad: incluir en el PR la referencia al dictamen y enlazar al archivo en `docs/legal/`.  
- Priorizar la protección del producto y la minimización del riesgo reputacional y económico.  

