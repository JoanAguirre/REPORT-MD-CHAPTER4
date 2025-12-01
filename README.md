# Evaluación de Experiencia de Usuario según Heurísticas – Sendify Dashboard

## Anexo D. Evaluación de User Experience
UX Heuristics & Principles Evaluation  
Usability – Inclusive Design – Information Architecture

Carrera: Ingeniería de Software 
Cliente(s): Sendify

---

## Sitio o aplicación evaluada  
Sendify – Shipments Dashboard

---

# Tareas evaluadas

El análisis se centra en evaluar la usabilidad de las tareas principales que los usuarios deben realizar dentro del dashboard. Las tareas evaluadas en esta revisión son:

1. Visualización del estado general de los envíos (Total, In transit, Delivered, Pending).  
2. Creación de un nuevo envío.  
3. Creación de un nuevo courier.  
4. Búsqueda de envíos por código de tracking.  
5. Aplicación de filtros por estado (Status).  
6. Aplicación de filtros por courier (Courier).  
7. Navegación mediante paginación en la tabla de envíos.  
8. Acceso a la opción de cambio de idioma.

### Tareas no consideradas en esta versión del análisis
1. Edición de envíos registrados.  
2. Eliminación de envíos.  
3. Visualización detallada de cada envío individual.  
4. Gestión de perfil del usuario.  
5. Configuraciones avanzadas del sistema.

---

# Escala de severidad utilizada

La evaluación de severidad para cada problema identificado se ha realizado según la siguiente escala:

| Nivel | Descripción |
|-------|-------------|
| 1 | Problema superficial, fácil de pasar por alto o superar. No requiere atención inmediata. |
| 2 | Problema menor, con impacto moderado. Debe considerarse para futuras mejoras. |
| 3 | Problema mayor. Puede afectar el flujo de trabajo y requiere ser corregido con prioridad. |
| 4 | Problema crítico. Impide el uso normal de la herramienta. Debe corregirse antes de liberar la aplicación. |

---

# Resumen de hallazgos

| Nº | Problema identificado | Severidad | Heurística o principio afectado |
|----|------------------------|-----------|--------------------------------|
| 1 | El selector de idioma (“English”) no se percibe claramente como un elemento interactivo. | 2 | Usability: Reconocimiento antes que recuerdo / Visibilidad de controles |
| 2 | Los filtros de la tabla (“Status” y “Courier”) no muestran adecuadamente si están activos. | 3 | Usability: Visibilidad del estado del sistema / Consistencia y estándares |

---

# Descripción detallada de problemas

---

## Problema 1: El selector de idioma no se percibe claramente como interactivo

**Severidad:** 2  
**Heurística comprometida:** Reconocimiento antes que recuerdo / Visibilidad de elementos interactivos

### Descripción
En la esquina inferior derecha del dashboard se incluye un control con la etiqueta "English". Su apariencia actual se asemeja a un texto estático o una simple etiqueta informativa. La falta de señales visuales de interactuación (como un borde, iconografía, estilo de botón o contraste diferencial) dificulta que el usuario identifique que dicho elemento permite cambiar el idioma del sistema.

Este comportamiento puede generar confusiones o pasar desapercibido, especialmente en usuarios que buscan explícitamente opciones lingüísticas o esperan encontrarlas en un lugar más convencional, como la parte superior de la interfaz.

### Recomendaciones
- Modificar el estilo visual del selector de idioma para que tenga el aspecto de un botón o un control desplegable.  
- Incluir un ícono asociado al idioma o a la configuración.  
- Reubicarlo en la barra superior del dashboard, siguiendo patrones estándar de interfaces web de tipo administrativo.  
- Garantizar que el componente responda visualmente al estado de hover y clic.

---

## Problema 2: Falta de visibilidad sobre los filtros activos en la tabla de envíos

**Severidad:** 3  
**Heurística comprometida:** Visibilidad del estado del sistema / Consistencia y estándares

### Descripción
La tabla de envíos permite filtrar los resultados mediante dos listas desplegables: "Status" y "Courier". Sin embargo, una vez aplicado un filtro, el sistema no proporciona retroalimentación clara que indique qué valores están siendo utilizados. Esto incluye:

- Ausencia de indicadores visuales de que un filtro está activo.  
- Falta de etiquetas, chips o textos que indiquen el criterio aplicado.  
- No se muestra un mensaje que informe al usuario cuántos resultados se están filtrando.  
- No se distingue visualmente entre un dropdown sin seleccionar y uno con un filtro activo.

La falta de claridad puede generar incertidumbre sobre si la vista actual refleja todos los envíos o solamente aquellos filtrados.

### Recomendaciones
- Añadir etiquetas o chips que indiquen explícitamente los filtros aplicados.  
- Incorporar un mensaje informativo, como “Resultados filtrados por: Status = In transit, Courier = Pablo”.  
- Modificar el estilo del dropdown cuando un filtro esté activo, diferenciándolo del estado por defecto.  
- Mostrar un mensaje como “Mostrando X resultados filtrados” para mejorar la visibilidad del estado del sistema.  

---

# Conclusiones generales

La evaluación evidenció que las áreas que requieren mayor atención están relacionadas con la visibilidad y claridad del estado del sistema. Aunque el dashboard de Sendify tiene una estructura ordenada y funciones claras, ciertos elementos no entregan suficiente retroalimentación visual, lo que puede dificultar la comprensión de la interfaz, especialmente para usuarios nuevos o en contextos de trabajo con alta carga de información.

Las recomendaciones realizadas apuntan a mejorar la transparencia de la interfaz, reforzar los elementos interactivos y asegurar que los usuarios tengan claridad sobre los filtros y opciones activas en todo momento.
