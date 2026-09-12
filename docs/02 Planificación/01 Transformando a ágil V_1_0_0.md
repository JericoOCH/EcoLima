# Transformando a ágil

## A. Metodología de Transformación

### 1. Requerimientos Funcionales (RF)

Los Requerimientos Funcionales (RF) de EcoLogística Lima se transformarán a una estructura ágil mediante su agrupación en Épicas y posterior descomposición en Historias de Usuario (US). El proyecto cuenta con 11 Requerimientos Funcionales, desde RF-001 hasta RF-011, relacionados con la gestión de flota, pedidos, optimización y visualización de rutas, sostenibilidad, conductores, clientes y autenticación.

La transformación seguirá la siguiente estructura:

**Requerimiento Funcional → Épica → Historia de Usuario → Criterios de Aceptación**

Los RF que pertenezcan a una misma capacidad o área funcional podrán agruparse dentro de una misma Épica. Posteriormente, cada Épica será dividida en Historias de Usuario que representen funcionalidades concretas y manejables para los usuarios del sistema.

Para realizar esta transformación se considerarán los siguientes criterios:

- **Agrupación por funcionalidad:** se relacionarán los RF que pertenezcan a una misma capacidad del sistema.
- **Identificación del usuario:** cada Historia de Usuario se asociará con el actor que utiliza o se beneficia de la funcionalidad.
- **Descomposición:** cuando un RF incluya varias operaciones diferenciadas, podrá dividirse en varias Historias de Usuario.
- **Trazabilidad:** cada Historia de Usuario deberá mantener la relación con el RF que le dio origen.
- **Reglas de negocio:** se considerarán las reglas de negocio asociadas a cada RF para asegurar que las Historias de Usuario representen correctamente las condiciones del sistema.
- **Priorización:** se tendrá en cuenta la prioridad definida para cada RF, dando especial atención a los requisitos clasificados como de prioridad Alta.

Los actores utilizados para redactar las Historias de Usuario serán principalmente Administrador, Operador/Técnico Logístico, Conductor, Auditor Externo y Usuario Final/Cliente, identificados como usuarios directos del sistema.

La descomposición de un RF podrá realizarse cuando este contenga varias funcionalidades que puedan gestionarse de manera independiente. Por ejemplo, RF-001 contempla el registro, actualización, consulta y deshabilitación lógica de vehículos, por lo que estas operaciones pueden convertirse en Historias de Usuario independientes cuando resulte conveniente para facilitar su desarrollo y seguimiento.

La transformación mantendrá la trazabilidad mediante una relación como la siguiente:

**RF-001 → EP-01 → US-001**

De esta forma, será posible identificar qué requisito funcional dio origen a cada Épica e Historia de Usuario.

Asimismo, las reglas de negocio asociadas a los requisitos serán consideradas durante la definición de las Historias de Usuario y sus criterios de aceptación. Por ejemplo, la generación de rutas (RF-003) está condicionada por reglas relacionadas con emisiones de CO₂, jornadas y descansos de los conductores, ventanas de tiempo, capacidad de los vehículos, prioridades de pedidos y restricciones ambientales.

Finalmente, cada Historia de Usuario será revisada para verificar que:

- Corresponda a un RF existente.
- Tenga un usuario o rol claramente identificado.
- Represente una funcionalidad concreta.
- Pertenezca a una Épica.
- Mantenga trazabilidad con el requisito original.
- Considere las reglas de negocio relacionadas.
- Pueda ser validada mediante criterios de aceptación.

Con esta metodología, los Requerimientos Funcionales se convertirán en elementos de trabajo más pequeños y comprensibles, facilitando su organización posterior en el Product Backlog y su gestión mediante Jira.

### 2. Requerimientos No Funcionales (RNF)

Los Requerimientos No Funcionales (RNF) se transformarán principalmente en Historias Técnicas (Enablers) cuando requieran un trabajo específico de infraestructura, arquitectura, seguridad, rendimiento o calidad. Cuando un RNF pueda verificarse directamente sobre una funcionalidad, se incorporará como Criterio de Aceptación o como parte de la Definition of Done (DoD). El proyecto cuenta con 10 RNF relacionados con rendimiento, seguridad, disponibilidad, escalabilidad, usabilidad, compatibilidad, mantenibilidad, eficiencia, precisión y privacidad.

La transformación seguirá este criterio:

**RNF → Enabler técnico / Criterio de Aceptación / DoD**

| RNF | Tratamiento ágil |
|---|---|
| RNF-001 Rendimiento | Enabler técnico + criterios de aceptación |
| RNF-002 Seguridad | Enabler técnico + DoD |
| RNF-003 Disponibilidad | Enabler técnico |
| RNF-004 Escalabilidad | Enabler técnico |
| RNF-005 Usabilidad y accesibilidad | Criterios de aceptación + DoD |
| RNF-006 Compatibilidad | Criterios de aceptación |
| RNF-007 Mantenibilidad | DoD |
| RNF-008 Eficiencia | Enabler técnico + criterios de aceptación |
| RNF-009 Precisión funcional | Criterios de aceptación |
| RNF-010 Privacidad | Enabler técnico + DoD |

Por ejemplo, RNF-001 puede generar una Historia Técnica relacionada con mejorar el rendimiento de la optimización de rutas, mientras que RNF-005 puede aplicarse como criterio de aceptación en las historias relacionadas con las interfaces del sistema.

Los Enablers tendrán una estructura sencilla:

> Como equipo técnico, queremos [realizar una mejora técnica], para [cumplir una necesidad de calidad del sistema].

**Ejemplo:**

> **EN-001:** Como equipo técnico, queremos optimizar el procesamiento de las rutas, para que la generación de rutas cumpla con el tiempo de respuesta establecido.

La transformación permitirá mantener los RNF presentes en el Product Backlog sin convertir cada requisito de calidad en una historia funcional independiente. Además, facilita su seguimiento y validación durante el desarrollo mediante criterios de aceptación y la DoD.

## B. Estructura Estándar de Historias de Usuario (US)

Cada Historia de Usuario (US) será redactada utilizando una estructura uniforme que permita identificar claramente al usuario, la funcionalidad solicitada y el valor que esta aporta al proyecto.

La estructura establecida será:

```text
ID: US-001

Título: [Título descriptivo]

Épica Relacionada: EP-01 [Nombre de la Épica]

Redacción:

Como [Rol / Tipo de Usuario],

quiero [Acción / Funcionalidad deseada],

para [Beneficio / Valor de Negocio esperado].
```

Para mantener la calidad y trazabilidad de las historias, cada US deberá:

- Tener un ID único.
- Contar con un título claro y descriptivo.
- Estar relacionada con una Épica.
- Identificar un rol o tipo de usuario.
- Describir una acción o funcionalidad concreta.
- Expresar el beneficio o valor de negocio esperado.
- Mantener correspondencia con el Requerimiento Funcional (RF) de origen.
- Considerar las reglas de negocio que correspondan.

Esta estructura será utilizada para las Historias de Usuario que conformarán el Product Backlog de EcoLogística Lima.

## C. Criterios de Aceptación bajo Sintaxis BDD (Gherkin)

Toda Historia de Usuario (US) y cada Enabler deberá contar con al menos **dos (2) Criterios de Aceptación**, utilizando la sintaxis BDD (Gherkin) para describir de manera clara y verificable el comportamiento esperado del sistema.

Cada criterio seguirá la siguiente estructura:

```text
Escenario: [Título descriptivo del escenario]

Dado [Contexto previo o precondición del sistema]

Cuando [Acción o evento ejecutado por el usuario o sistema]

Entonces [Resultado esperado o estado final verificable]
```

Los criterios deberán:

- Estar relacionados directamente con la US o Enabler correspondiente.
- Describir condiciones que puedan ser comprobadas.
- Utilizar situaciones claras y realistas para el alcance del proyecto.
- Considerar las reglas de negocio cuando correspondan.
- Incluir como mínimo dos escenarios por cada US o Enabler.

Estos criterios servirán posteriormente para validar las Historias de Usuario y Enablers durante su implementación y seguimiento en Jira.

## D. Definition of Done (DoD) Global del Proyecto

Una Historia de Usuario (US) o Enabler se considerará **Done** cuando cumpla con todos los siguientes criterios de calidad:

- **Pruebas unitarias:** se alcanza una cobertura de pruebas unitarias **≥ 80%**.
- **Análisis de código:** el análisis estático mediante SonarQube o CodeQL no presenta vulnerabilidades críticas.
- **Revisión de código:** el código cuenta con un Peer Review aprobado por al menos un integrante técnico, realizado mediante un Pull Request.
- **Despliegue:** la funcionalidad puede ser desplegada de forma automatizada en el ambiente de Staging/Pruebas.
- **Documentación:** la documentación de la API o del código relacionado se encuentra actualizada, utilizando OpenAPI/Swagger cuando corresponda.
- **Criterios de aceptación:** se cumplen los criterios de aceptación definidos mediante Gherkin para la US.
- **Integración:** la funcionalidad se encuentra integrada correctamente con el código existente y no genera errores en las pruebas realizadas.

**Regla general:** si alguno de los criterios anteriores no se cumple, la Historia de Usuario no podrá considerarse Done y deberá permanecer en el estado correspondiente hasta completar las condiciones pendientes.
