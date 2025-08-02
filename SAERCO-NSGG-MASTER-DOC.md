# SAERCO-NEW-SGG-MASTER-DOC

## 1. Propósito del documento

Este documento establece la visión estratégica, técnica y organizativa para la evolución del Sistema General de Gestión (SGG) de SAERCO hacia una arquitectura moderna, modular, trazable, y plenamente compatible con tecnologías de inteligencia artificial (IA).

### Este documento es:

- Una **guía viva y versionada** para transformar la gestión documental de SAERCO.
- El punto de partida para alinear herramientas, procesos y equipos bajo un enfoque digital, semántico y automatizable.
- La base para construir un ecosistema documental interoperable con modelos de lenguaje (LLMs) y sistemas de búsqueda inteligentes.

Este documento está destinado tanto a perfiles técnicos como no técnicos, y será acompañado por guías de estilo, estructura de carpetas, ejemplos de metadatos, control de versiones y herramientas recomendadas para su implementación y mantenimiento.

## 2. Estado actual del Sistema General de Gestión (SGG)

El Sistema General de Gestión (SGG) de SAERCO, en su versión actual, está basado en un ecosistema documental tradicional centrado en archivos Word (.docx) y PDF, almacenados y versionados manualmente en SharePoint. A lo largo del tiempo, el sistema ha acumulado una importante carga documental, estructurada funcionalmente pero limitada técnicamente para su explotación digital o automatización.

### 2.1 Formato y almacenamiento

- La mayoría de documentos se redactan y mantienen en Microsoft Word.
- Las versiones finales se exportan a PDF y se almacenan en carpetas por área/servicio dentro de SharePoint.
- El control de versiones se realiza mediante campos manuales dentro de los documentos y el nombre del archivo, sin un sistema de versionado centralizado o automatizado.

### 2.2 Tipología documental

El SGG se compone de:

- Manuales (MAN)
- Procedimientos (PRD)
- Instrucciones técnicas (IT)
- Formatos de registro (FORM)

Muchos de estos documentos incluyen contenido redundante (definiciones, normativa, tablas repetidas) y estructuras distintas dependiendo del autor o el área.

### 2.3 Control de versiones y trazabilidad

- El control de cambios se realiza dentro del propio documento Word, mediante tablas manuales o notas de revisión.
- Los documentos versionados no siempre siguen una convención de nombres clara, generando variantes como `final`, `revisado`, `v5.1_definitivo`, etc.
- No existe un repositorio centralizado ni un histórico consolidado de cambios a nivel de sistema.

### 2.4 Limitaciones actuales

El sistema presenta limitaciones significativas que dificultan su eficiencia y escalabilidad:

- ❌ Ausencia de estructura semántica legible por máquinas.
- ❌ Redundancia de contenido y falta de normalización.
- ❌ Baja trazabilidad interdocumental (por ejemplo, referencias a normativa o formatos no están enlazadas ni son navegables).
- ❌ Dificultad para generar conocimiento automatizado o búsquedas inteligentes.
- ❌ Incompatibilidad práctica con modelos de lenguaje (LLMs), IA documental o sistemas de búsqueda semántica.

### 2.5 Necesidad de transformación

La creciente complejidad operativa, la necesidad de trazabilidad normativa, y el potencial de uso de modelos de lenguaje exigen una transformación profunda del SGG. Esta transformación permitirá:

- Reducción del esfuerzo manual.
- Aumento de la fiabilidad documental.
- Posibilidad de consultar el SGG por lenguaje natural.
- Preparación del ecosistema documental para su integración futura con asistentes inteligentes, buscadores semánticos y análisis automatizados.

## 3. Objetivos estratégicos

La transformación del Sistema General de Gestión (SGG) de SAERCO responde a una visión estratégica orientada a posicionar la organización a la vanguardia de la gestión documental regulada, aprovechando tecnologías emergentes como los modelos de lenguaje (LLMs), la automatización semántica y el versionado estructurado.

Los objetivos estratégicos del nuevo SGG son los siguientes:

### 3.1 Compatibilidad con IA y modelos de lenguaje (LLMs)

- Estructurar el contenido en formatos legibles por máquina (Markdown + metadatos YAML).
- Eliminar el ruido documental (índices automáticos, marcas de estilo, campos ocultos).
- Permitir la explotación del contenido por sistemas de consulta semántica, resúmenes automáticos y generación de conocimiento.

### 3.2 Trazabilidad normativa y documental

- Establecer vínculos explícitos entre procedimientos, instrucciones técnicas y normativa aplicable.
- Incluir referencias formales a reglamentos europeos (R373, R340...), políticas internas y definiciones centralizadas.
- Garantizar la auditabilidad y demostrabilidad del cumplimiento.

### 3.3 Automatización del control de versiones

- Sustituir el control manual de versiones por versionado semántico basado en Git.
- Generar automáticamente tablas de versiones a partir del historial del repositorio.
- Facilitar la revisión, comparación y validación de cambios.

### 3.4 Estandarización y reutilización

- Establecer una guía de estilo para homogeneizar la redacción, estructura y navegación de los documentos.
- Reutilizar componentes comunes (definiciones, normativa, autores) mediante inclusión modular (`!include` o enlaces internos).
- Minimizar el contenido duplicado en el sistema.

### 3.5 Accesibilidad y navegabilidad

- Ofrecer una experiencia de lectura clara, navegable y jerárquicamente coherente para usuarios técnicos y no técnicos.
- Implementar sistemas de navegación visual (GitBook, Docusaurus) y organización por área/proceso.
- Asegurar el acceso controlado, según perfil y nivel de confidencialidad.

### 3.6 Escalabilidad, sostenibilidad y mantenimiento

- Permitir que el sistema crezca sin perder estructura ni coherencia.
- Hacerlo sostenible para ser mantenido por diferentes equipos sin depender de conocimientos técnicos profundos.
- Preparar la base documental para integración futura con IA organizacional, asistentes internos o plataformas regulatorias.

## 4. Principios de diseño del nuevo SGG

La transformación del Sistema General de Gestión no es únicamente tecnológica, sino también conceptual. El nuevo SGG debe construirse sobre una base sólida de principios que garanticen su utilidad operativa, su compatibilidad regulatoria y su apertura a la inteligencia artificial. Estos principios son los pilares que guían todas las decisiones de arquitectura, formato, estructura y despliegue.

### 4.1 Modularidad

- Cada documento debe representar una unidad funcional, claramente delimitada (manual, procedimiento, instrucción...).
- El contenido común se desacopla en módulos reutilizables (definiciones, normativa, formatos).
- Los documentos pueden componerse o vincularse entre sí de forma jerárquica o transversal.

### 4.2 Estructura semántica

- Toda la información debe estar estructurada de forma que pueda ser comprendida tanto por humanos como por modelos de lenguaje.
- El contenido se representa mediante Markdown para la redacción y YAML para los metadatos.
- Se establecen convenciones claras para títulos, listas, tablas, referencias y enlaces.

### 4.3 Trazabilidad y auditabilidad

- Cada documento mantiene su historial de cambios mediante control de versiones Git.
- Las referencias normativas, reglamentarias y operativas están registradas de forma explícita.
- Se puede reconstruir fácilmente qué versiones estuvieron activas en cada momento y qué cambios se hicieron.

### 4.4 Normalización

- El nuevo SGG se apoya en una guía de estilo que regula el uso de encabezados, estructura, nomenclatura, formatos visuales y sintaxis.
- Se unifican criterios de nomenclatura de archivos y carpetas, tanto para humanos como para herramientas automáticas.
- La documentación será coherente en forma, lenguaje y diseño en toda la organización.

### 4.5 Accesibilidad y navegabilidad

- La información debe ser navegable y visualmente clara para cualquier perfil profesional.
- Se prioriza la lectura directa desde GitHub o desde interfaces como GitBook o Docusaurus.
- Se proporciona un sistema de navegación estructurada, sin necesidad de conocimientos técnicos.

### 4.6 Compatibilidad y sostenibilidad

- Todo el sistema debe poder mantenerse con herramientas estándar (Git, Markdown, editores de texto, validadores).
- No debe depender de soluciones propietarias cerradas ni de expertos altamente especializados.
- Debe poder evolucionar hacia la integración con IA, sin requerir rediseños de fondo.

## 5. Arquitectura documental

El Sistema General de Gestión (SGG) de SAERCO se articula a través de una arquitectura documental jerárquica y funcional, compuesta por manuales, procedimientos, instrucciones técnicas y formatos de registro. Esta estructura permite garantizar la coherencia organizativa, el cumplimiento normativo y la mejora continua de los procesos.

La evolución del SGG hacia una nueva arquitectura basada en Markdown y control de versiones (NSGG) se apoyará en esta base actual, manteniendo su lógica jerárquica, pero incorporando modularidad, semántica estructurada y trazabilidad digital.

---

### 5.1 Tipos documentales en el SGG actual

Tal como se establece en el apartado 3.1 del Manual del SGG:

- **Manuales (MAN):** documentos de nivel superior que establecen las directrices, políticas y responsabilidades en cada área (Calidad, SGSO, Seguridad Física, RRHH, Formación, etc.).
- **Procedimientos (PRD):** describen de forma sistemática quién, cómo, cuándo y con qué medios se ejecuta una función.
- **Instrucciones Técnicas (IT):** desarrollan aspectos específicos de los procedimientos, con carácter eminentemente técnico.
- **Formatos:** documentos normalizados para recoger información. Una vez cumplimentados, se consideran registros.
- **Documentos externos:** normativa legal, métodos, publicaciones técnicas, etc., cuya aplicación afecta a los procesos internos.

---

### 5.2 Relación jerárquica entre documentos

La arquitectura documental actual se basa en una **estructura piramidal**:


MANUAL DEL SGG

┌─────────────┼─────────────┐

PROCEDIMIENTOS       INSTRUCCIONES FORMATOS
                                │
                      REGISTROS DEL SISTEMA

Cada nivel documental desarrolla o evidencia el nivel anterior.

---

### 5.3 Estructura de almacenamiento actual

Los documentos se almacenan actualmente en SharePoint, en carpetas por área o servicio, en formatos `.docx` y `.pdf`. El control de versiones se realiza:

- Dentro del propio documento (en tablas de revisión).
- En el nombre del archivo (con convenciones no homogéneas).
- Mediante control de cambios en Word.

Esta estructura, aunque funcional, **limita la trazabilidad automática, la normalización y la integración con tecnologías de IA**.

---

### 5.4 Evolución prevista: arquitectura del NSGG

La evolución hacia la nueva arquitectura documental tendrá en cuenta la base actual, y se fundamentará en:

- Organización por **tipo documental** y/o **área funcional**.
- Cada documento vivirá en una **carpeta propia**, con:
  - `metadata.yaml`: metadatos clave
  - `contenido.md`: cuerpo principal del documento
  - `historial.md`: cambios relevantes
  - `anexos/`: documentos relacionados
- Existencia de repositorios comunes para:
  - **Definiciones**
  - **Normativa vinculante**
  - **Formatos reutilizables**

---

### 5.5 Transición y compatibilidad

Durante la transición se mantendrán mecanismos de compatibilidad entre versiones antiguas y nuevas:

- Inclusión de enlaces a documentos históricos en PDF cuando sea necesario.
- Mantenimiento de códigos actuales (`SSSCC-AREA-TIPO-XX`) como identificadores únicos.
- Conservación de la trazabilidad normativa y los vínculos interdocumentales.

---

## 6. Guía de estilo y estructura de contenido

Para garantizar la coherencia, legibilidad, trazabilidad y compatibilidad con modelos de lenguaje, todo documento del nuevo Sistema General de Gestión (NSGG) seguirá una estructura y estilo común. Esta guía de estilo es obligatoria para todos los documentos que se integren al repositorio documental en Markdown.

---

### 6.1 Jerarquía de encabezados

- Se utilizarán como máximo **tres niveles de encabezado**:
  - `##` para secciones principales
  - `###` para subsecciones
  - `####` para subapartados (uso excepcional)
- No se utilizarán encabezados `#` de primer nivel (reservado para el título del documento).
- Se evitará el uso de negrita para encabezados. Solo Markdown nativo (`##`).

---

### 6.2 Convención para las secciones

Cada documento deberá estructurarse, al menos, con los siguientes bloques:

1. Objetivo
2. Alcance
3. Definiciones (si aplica)
4. Responsabilidades
5. Desarrollo / Procedimiento / Contenido
6. Referencias normativas y documentales
7. Anexos (si aplica)

---

### 6.3 Normas de estilo para el contenido

- Evitar estructuras visuales complejas heredadas de Word (tablas multicolumna, sangrías, etc.).
- No usar mayúsculas sostenidas en encabezados ni listas.
- El lenguaje debe ser técnico, claro y directo.
- Incluir enlaces a otros documentos mediante rutas relativas (`[Ver PRD03](../procedimientos/NSGG-PRD-03/README.md)`).

---

### 6.4 Tablas

- Toda tabla deberá tener:
  - Un título encima con formato: `**Tabla X.Y – Descripción**`
  - Encabezado alineado a la izquierda.
  - Separador horizontal claro (`| --- |`).
- Evitar tablas anidadas o tablas con celdas fusionadas.
- No usar tablas para maquetación visual. Solo para datos.

---

### 6.5 Imágenes, diagramas y gráficos

- Todas las imágenes deberán almacenarse en una carpeta `assets/` dentro del directorio del documento correspondiente.
- Se recomienda usar HTML básico para centrar la imagen dentro del documento Markdown.
- Las imágenes deben estar acompañadas por un pie de figura situado inmediatamente debajo.

Ejemplo:

\```
<p align="center">
  <img src="./assets/diagrama-flujo.png" alt="Diagrama de flujo" width="600"/>
</p>```

- Las imágenes deben llevar un pie explicativo inmediatamente debajo, con formato:

**Figura X.Y – Descripción de la imagen**

## ⚠️ Importante

- No pongas el bloque HTML suelto *fuera* de las triple comillas invertidas \(```html ... ```\) si quieres mostrarlo como ejemplo.
- GitHub y GitBook **sí interpretan el HTML si no está en bloque de código**.

---

### 6.6 Referencias normativas

Las referencias a reglamentos, normas ISO u otros documentos deben usar un formato normalizado:
[R373/2017, art. 5] o [ISO9001:2015, sección 8.4.3]

Si existe un repositorio de normativa vinculado (/reglamento/), enlazar a él.

---

### 6.7 Reutilización de contenido común

Para evitar duplicidad y facilitar la actualización:

Definiciones, abreviaturas y acrónimos comunes estarán centralizadas en un documento único (/glosario/definiciones.md).

Cada documento debe enlazar (no repetir) contenido ya definido.

Los bloques de contenido reutilizable (como normativa recurrente) podrán referenciarse por enlace o incluirse por plantillas en el futuro (!include, si se automatiza).

---

### 6.8 Licencia y pie legal

Todos los documentos incluirán al final una cláusula legal estandarizada:


© 2025 SAERCO, Servicios Aeronáuticos, Control y Navegación S.L.  
Todos los derechos reservados. Ver archivo [LICENSE](./LICENSE) para más información.

---

## 7. Control de versiones y trazabilidad

El nuevo Sistema General de Gestión (NSGG) se basará en un control de versiones técnico y transparente, respaldado por Git. Esta infraestructura permitirá trazar con precisión la evolución de cada documento, vincular los cambios con sus responsables, y automatizar la generación de tablas de versiones y revisiones.

---

### 7.1 Versionado mediante Git

Todo el repositorio documental se gestionará mediante Git, lo que garantiza:
  - Registro cronológico de cada modificación.
  - Identificación del autor de cada cambio.
  - Restauración de versiones anteriores en cualquier momento.

Las versiones ya no se reflejarán en el nombre del archivo (como `v5.6`), sino que se mantendrán en el historial Git y en los metadatos YAML del documento.

---

### 7.2 Metadatos de versión

Cada documento contendrá un archivo `metadata.yaml` donde se incluirán campos como:

\```yaml
versión: "1.0"
fecha: "2025-08-05"
redactado_por: "Especialista"
revisado_por: "Director de Calidad"
aprobado_por: "Director General"
estado: "En vigor"

Estos datos podrán ser leídos por sistemas automatizados para generar resúmenes, tablas de control o informes de cumplimiento.

---

### 7.3 Historial interno del documento

Opcionalmente, se podrá mantener un archivo `historial.md` para registrar cambios significativos de manera legible por humanos:

| Versión | Fecha      | Cambios realizados                     |
| ------- | ---------- | -------------------------------------- |
| 1.0     | 2025-08-05 | Creación del procedimiento             |
| 1.1     | 2025-09-12 | Actualización de anexos y definiciones |

---

7.4 Tabla de control de versiones centralizada

A nivel del repositorio, se podrá mantener un archivo maestro de versiones (versiones.csv o .yaml) que relacione:

- Código del documento
- Última versión
- Fecha
- Estado (borrador, aprobado, obsoleto)
- Responsable

Ejemplo (CSV):

Código,Versión,Fecha,Estado,Responsable
NSGG-PRD-03,1.1,2025-09-12,En vigor,Director de Calidad
NSGG-MAN-CALIDAD,1.0,2025-08-05,En vigor,Director General

---


### 7.5 Rastreabilidad normativa

Cada documento deberá declarar claramente:

- Las normas y reglamentos que aplica o desarrolla.
- Las secciones o artículos específicos a los que da cumplimiento.
- Los vínculos con documentos complementarios (por ejemplo, manuales o ITs relacionados).

Esta trazabilidad podrá integrarse en el `metadata.yaml` o en una sección específica del contenido.

### 7.6 Identificación unívoca de documentos

Cada documento contará con un identificador único con la siguiente estructura:

NSGG-<TIPO>-<CÓDIGO>-<NOMBRE>

Ejemplos:

- NSGG-PRD-03-GESTION-MEJORA
- NSGG-MAN-CALIDAD
- NSGG-IT-04-EVALUACION-RIESGOS




© 2025 SAERCO, Servicios Aeronáuticos, Control y Navegación S.L.  
Todos los derechos reservados. Ver archivo [LICENSE](./LICENSE) para más información.
