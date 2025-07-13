# Entender el Problema

## Product discovery 
`_build the right thing_ ✅ :ok ≠ _build the thing right_ ❌`

El product discovery implica ciertas tecnicas:
- entrevistas a clientes
- customer journey
- mapa de empatia

## Tecnicas de innovacion 
### Design thinking
Para generar ideas innovadoras, que centra su eficacia en entender y dar solución a las necesidades reales de los usuarios.

**{ empatizar -> definir -> idear -> prototipar -> testear }**

|Empatizar|Definir|Idear|Prototipar|Testear|
|---------|-------|-----|----------|-------|
|**Exploramos el contexto**: comprensión de las necesidades. Investigación cuali/cuantitativa |**Detectamos oportunidades**: patrones de conducta, insights, oportunidades de innovación|**Proponemos soluciones** según el contexto y las necesidades. Pensamiento divergente. BrainStorming. |**Seleccionamos la idea con la mejor propuesta de valor**, y la convertimos en un prototipo.|Hacemos parte al usuario. **Co-creamos en base a la prueba y error**|

Los beneficios son:
- Reduce el riesgo.
- Mejora la calidad.
- Aborda las necesidades reales.
- Fomenta la innovación al explorar múltiples vías para el mismo problema.
- Convierte los problemas en oportunidades.
- Fomenta el trabajo en equipo (multidisciplinario).
- Mejora la empatía en la cultura empresarial.
- Se obtiene resultados tangibles y consistentes.

### Pensamiento divergente y convergente
- Pensamiento divergente: creativo, explorativo. Implica generar múltiples soluciones a un problema explorando diversas perspectivas y posibilidades. Fomenta la creatividad y la innovación al desafiar el pensamiento convencional y explorar soluciones no convencionales
- Pensamiento convergente: logico y analitico. Implica evaluar y seleccionar la mejor solución entre las opciones generadas a través del pensamiento divergente. Requiere análisis crítico y toma de decisiones para identificar la solución más efectiva al problema.

### BrainStorming 
Es útil recurrir a esta técnica cuando se necesita mejorar a partir de la creatividad, el planteamiento de muchas ideas alternativas, conceptos nuevos.

Fundamentalmente toda critica esta prohibida, toda y tantas ideas como sea posible son bienvenidas, ademas el desarrollo y asociación de las ideas es deseable (resonancia selectiva).

<div style="page-break-after: always;"></div>

# Outcomes vs Outputs 
El efecto que genera _vs_ lo que se entrego. Lo que importa es el valor que se genera a partir de lo que entregamos.

Un **output** es un entregable, una actividad concreta. Algo que se construye o se hace.

Un **outcome** es un cambio de comportamiento que impulsa resultados de negocio.

|Recursos|Actividades|Outputs|Outcomes|Impacto|
|--------|-----------|-------|--------|-------|
|Planificamos nuestros recursos|Llevamos a cabo un conjunto de actividades preparativas|Si todo esto sale según lo planeado, creamos el output|Si funciona según lo planeado, logramos nuestro outcome|Esto, a su vez, "contribuye" directamente al impacto que buscamos|

Hay que gestionar un proyecto segun outcomes definidos en terminos de comportamientos humanos especificos, generando una forma de trabajar centradas totalmente en el cliente y en el usuario.

## Hipotesis
No podemos asumir que lo que entregamos generará automáticamente valor. Para reducir la incertidumbre, utilizamos hipótesis.

Una hipótesis básica tiene dos partes:

- **La idea**: Lo que creemos que es cierto.
- **La evidencia**: Lo que necesitamos medir para validarlo

Para validar esta hipótesis, necesitamos definir métricas clave: las métricas nos permiten evaluar si los outcomes esperados realmente están ocurriendo. Mide el exito.

<div style="page-break-after: always;"></div>

# Clean Code

### Nombres
- Nombres significativos y pronunciables, en variables por ejemplos
- Nombres que revelen su intencion, de una funcion por ejemplo
- Uso de notaciones, aunque hoy no hace falta porque los IDEs son mas inteligentes
- Evitar uso de datos hardcodeados

### Funciones
- Funciones/Metodos pequeños
- Hacer una sola cosa: _Single Responsibility Principle_
- Un solo nivel de abstraccion por funcion: reducir tamaño de funciones y hacer una sola cosa por funcion
- Poder leer de arriba para abajo

### Logica
- Evitar switch: rompe la regla de solamente una cosa
- Argumentos: uno es bueno, cero mejor.
- Flag (parámetro bool que se pasa a una función para cambiar su comportamiento): es preferible usar polimorfismo o crear nuevas funciones.
- DRY Principle: no repetirse
- The Principle o Least Surprise: el código debe comportarse de la forma en que se esperaria
- The Boy Scout Rule: deja el código más limpio de lo que lo encontraste

### Comentarios
- Un comentario que explica todo, es malo
- Comentarios legales, informativos o explicativos de una intencion, depende si es que son correctos o no
- Advertencias de consecuencias (x test tarda mucho), TODO (tarea a realizar), ampliar informacion, con comentarios buenos.
- Malos comentarios son los redundantes (al pedo), erroneos, comentarios de tipo Diario, codigo comentado (muerto).

### Excepciones
- Usar excepciones en vez de mensajes de error

### Tests Unitarios
Tests **F.I.R.S.T.**
- Fast
- Independent
- Repeatable
- Self-Validating
- Timely

Son casos de prueba aislados, prueba una sola cosa por test, un unico metodo de assert por cada caso.


<div style="page-break-after: always;"></div>

# Criterios de Buen Diseño

Analisis es acerca del **QUE** necesitamos

Diseño es acerca del **COMO** lo resolvemos

## Mal diseño:
- **Rigidez**: dificil de cambiar
- **Fragilidad**: el código es propenso a romperse cuando se hacen cambios. Pequeñas modificaciones pueden generar errores en partes inesperadas
- **Inmovilidad**: muy dependiente del resto, no te lo podes llevar
- **Viscosidad**: es más fácil escribir código malo que código bueno. Si el código limpio requiere mucho esfuerzo, se termina optando por soluciones rápidas y sucias

Se busca alta cohesion y bajo acoplamiento, poca dependencia entre cosas

## SOLID
**S** - Single Responsibility (SRP): mantenerlo simple. Una sola responsabilidad, hacer una sola cosa.<br>
**O** - Open/Closed (OCP): abierto a la extension, cerrado a la modificacion. Deberíamos poder agregar nuevas funcionalidades sin modificar el código existente.<br>
**L** - Liskov Substitution (LSP): Las subclases deben poder reemplazar a sus clases padre sin romper el código. Si una clase hereda de otra, debe poder ser usada sin necesidad de modificar el código original<br>
**I** - Interface Segregation (ISP): Las interfaces deben ser específicas, no forzar a las clases a implementar métodos que no usan. <br>
**D** - Dependency Inversion (DIP): Las clases deben depender de abstracciones, no de implementaciones concretas. En lugar de que una clase dependa directamente de otra, es mejor que dependa de una abstracción (interfaz o clase base).<br>



<div style="page-break-after: always;"></div>

# Agilidad, Scrum, XP y Kanban

## Marco Cynefin 
Nos ofrece cinco dominios o contextos para la toma de decisiones: claro, complicado, complejo, caótico y desordenado que ayudan a los líderes a identificar cómo perciben las situaciones y entender su propio comportamiento, así como el de otras personas.<br>
Cada dominio representa una situación o entorno, cada uno con un nivel distinto de complejidad y previsibilidad en la relación causa-efecto. Estos dominios guían a las organizaciones sobre qué tipo de prácticas o enfoques son más adecuados para abordar los desafíos o problemas. <br>
1. **Simple (Obvio)**: Representa un entorno en el que las relaciones causa-efecto son obvias para todo el mundo. En este tipo de entornos se aplican procedimientos estándar y reglas bien establecidas que han demostrado ser efectivas y eficientes en este tipo de situaciones; las mejores prácticas son soluciones conocidas.
2. **Complicado**: Representa un entorno en el que es necesario un análisis o conocimiento experto para resolver problemas.En este dominio se buscan buenas prácticas. Implican análisis o intervención de expertos para entender la relación causa-efecto, que no es inmediatamente aparente pero es descifrable.
3. **Complejo**: Representa un entorno en el que la relación causa-efecto se comprende solo en retrospectiva. No hay respuestas inmediatas, en este dominio se buscan prácticas emergentes: soluciones que surgen a través de la experimentación y la interacción dentro del sistema.
4. **Caótico**: Representa un entorno en el que no hay relaciones causa-efecto claras. Esto genera urgencia y acción inmediata. Para ello se utilizan prácticas novedosas: acciones inmediatas y experimentales tomadas para establecer el orden
5. **Desorden**: Representa un estado de confusión donde no está claro en qué dominio se está operando. Actúa como una llamada de atención para diagnosticar la situación correctamente y moverse hacia el dominio correspondiente.
**VUCA** es un modelo de gestión de entornos complejos, volátiles, impredecibles y ambiguos
![Screenshot from 2025-03-17 19-31-28](https://github.com/user-attachments/assets/e7c3fba0-24ed-4c14-b240-cfe5b53c869f)

## Que es agilidad
La metodología Agile es un enfoque iterativo e incremental para la gestión de proyectos que prioriza la flexibilidad, la colaboración y la entrega continua de valor, en lugar de un enfoque rígido y planificado.

#### Que no es
No es una metodologia porque no pretende indicarnos que hacer paso a paso.<br>
No es ir mas rapido, aunque entregar valor temprano si es un de las promesas agiles.<br>
No es multitasking, aunque implique gestionar un contexto complejo, incierto y cambiante. No es necesario hacer todo a la vez. <br>

#### Que es
Es una forma de hacer que nos invita a experimentar y aprender en pasos pequenios.<br>
Es una forma de ser en la que nos ayudamos, nos cuidamos y mejoramos nuestro entorno.<br>
Son valores y principios.

## Scrum + Kanban + XP

**Kanban** es una metodología de gestión de proyectos que se basa en tableros visuales para organizar el trabajo. Es un método ágil.

#### Mecanismo agil iterativo incremental
Es una metodología de desarrollo de software que se basa en la entrega de incrementos funcionales del producto a lo largo del proyecto. 

En un desarrollo iterativo e incremental el proyecto se planifica en diversos bloques temporales (en el caso de Scrum de un mes natural o hasta de dos semanas, si así se necesita) llamados iteraciones.

Las iteraciones se pueden entender como miniproyectos: en todas las iteraciones se repite un proceso de trabajo similar (de ahí el nombre “iterativo”) para proporcionar un resultado completo sobre producto final, de manera que el cliente pueda obtener los beneficios del proyecto de forma incremental. 

En el **metodo tradicional** hay una entrega de valor unica al final pero en los metodos agile se basa en un desarrollo incremental, con entregas incrementales porque en cada iteracion se resolvio esa parte del problema.

![Screenshot from 2025-03-17 20-06-03](https://github.com/user-attachments/assets/99ce1808-1364-4ce0-9312-5fe0b5b004dd)

### XP (Extreme Programming)
Es una metodología ágil de desarrollo de software enfocada en la mejora continua, la colaboración estrecha y la entrega frecuente de software funcional. 

Es "extremo" porque todo se lleva al extremo las mejores prácticas del desarrollo de software. En lugar de aplicarlas ocasionalmente o de forma moderada, XP las maximiza para obtener mejores resultados.

![Screenshot from 2025-03-17 20-24-20](https://github.com/user-attachments/assets/357458ce-3eb3-4368-9254-214786e791f4)


## Corazon de la Agilidad
![Screenshot from 2025-03-17 20-51-22](https://github.com/user-attachments/assets/5368bf61-04d2-4b36-9f9d-22c905ae1481)

<div style="page-break-after: always;"></div>

# Scrum Framework
![scrum](https://github.com/user-attachments/assets/044cb01d-4e32-4311-bf24-fc8450c13830)

Scrum es un marco de trabajo ágil utilizado en el desarrollo de productos y proyectos. Se basa en ciclos cortos de trabajo llamados sprints, donde un equipo autoorganizado colabora para entregar incrementos funcionales del producto. Dentro de Scrum, existen diversas ceremonias que estructuran el trabajo y fomentan la mejora continua

## Roles
- **Product Owner**: Es la persona responsable de definir qué se debe hacer en el producto. Prioriza las tareas y gestiona el Product Backlog (lista de tareas). Es el puente entre el cliente y el equipo. Es quien recopila historias de usuario para el product backlog.

- **Scrum Master**: Es el facilitador del equipo, quiere que el equipo sea autonomo y organizado. Se asegura de que se sigan las reglas de Scrum, elimina obstáculos y ayuda a mejorar la forma de trabajar.

- **Development Team**: Son los desarrolladores y otros profesionales que trabajan en las tareas del Sprint para entregar un incremento del producto. Llevan a codigo el proyecto. Van a construir el producto

## Ceremonias de Scrum
Son reuniones estructuradas que ayudan a organizar el trabajo del equipo, fomentar la comunicación y mejorar continuamente el proceso de desarrollo. Son eventos clave dentro del marco de trabajo Scrum y garantizan que el equipo tenga alineación, planificación y retroalimentación constante.

Las ceremonias ágiles facilitan la comunicación entre los miembros del equipo y promueven una comprensión
compartida de lo que se está construyendo dentro de un sprint.

![image](https://github.com/user-attachments/assets/fc29d2af-4078-45b9-8502-88d4fb477289)

- **Sprint Planning**: Es la reunión inicial antes del Sprint. Se eligen historias del product backlog y se las completa para cargarlas en el sprint backlog donde ahi si van a estar priorizadas en tareas mas atomicas. En el sprint backlog resultante ya no hay caos. Las tareas ya están estimadas y el equipo conoce como realizarlas.
  - Colaboración del equipo para decidir cuánto tiempo se puede asignar al sprint.
  - Resumen del Product Owner sobre el resultado deseado para el sprint que se está planificando. Proporciona un objetivo compartido y explica por qué vale la pena emprender el sprint.
  -  Las historias de usuario se agregan al sprint backlog en base a un acuerdo colectivo del equipo. Esta es una oportunidad para que el equipo haga preguntas para aclarar lo que se pide en la historia de usuario si no se cubrió completamente en la refinación del backlog.
  -  Es un momento clave para inspeccionar y adaptarse. Alinea al equipo. Permita que todos puedan entender y compartir la vision del sprint

- **Daily Scrum**: Reunión breve diaria en la que el equipo sincroniza su progreso, comparte avances y detecta posibles obstáculos. No es una reunión de estado ni de reportes individuales, sino una oportunidad para coordinar el trabajo colaborativamente. El Scrum Master se asegura de que la reunión se lleve a cabo, pero los Desarrolladores son responsables de conducir el Daily Scrum. El Scrum Master trata de mantener el Daily Scrum
dentro del límite de tiempo de 15 minutos. El Daily Scrum es una reunión interna para el equipo Scrum. Cada miembro responde tres preguntas clave para alinear esfuerzos:
  -   ¿Qué hice ayer?
  -   ¿En qué trabajaré hoy?
  -   ¿Hay algún impedimento que me bloquee a mí o al equipo?

- **Sprint Review (Demo)**:  Es una reunión que se lleva a cabo el último día del sprint, donde el equipo Scrum muestra lo que ha logrado durante el sprint.
  - El equipo muestra a los stakeholders el trabajo que se realizo a lo largo del sprint.
  - Se invita a los asistentes a proporcionar retroalimentación sobre el trabajo actual y a sugerir cambios, los cuales se documentan para ser considerados.
  - El equipo tiene la libertad de presentar su trabajo de la manera que considere más adecuada, con el objetivo principal de dejar claro lo que se ha logrado durante el sprint y abrir el espacio para recibir retroalimentación y sugerencias de cambios necesarios.
  - El objetivo es la revision y retrioalimentacion sobre lo que se completo en el sprint, y comprension por parte de los stakeholders sobre lo que se completara en corto plazo.

 - **Sprint Retrospective**: Es una reflexion sobre el sprint al final del mismo. El equipo reflexiona sobre sus logros y dificultades durante el sprint, además de explorar oportunidades para mejorar continuamente el valor incremental que están proporcionando al producto El equipo se reune, debate y acuerda acciones. El objetivo es Obtener feedback de stakeholders y corregir el rumbo rápidamente. Algunas preguntas clave que pueden guiar una retrospectiva productiva incluyen: ¿Qué salió bien?, ¿Qué no salió bien?, ¿Qué podemos mejorar?. El objetivo es una reflexión sobre lo que el equipo está haciendo bien y lo que pueden mejorar, además de identificar los elementos clave en los que el equipo puede enfocarse para mejorar.

![image](https://github.com/user-attachments/assets/56783198-3954-4591-8844-3cd0e86dbdd9)

## Estimaciones
En Scrum, la estimación no busca ser exacta, sino útil para planificar. Se enfoca en determinar el esfuerzo relativo de las tareas para que el equipo pueda comprometerse con un volumen de trabajo realista en el Sprint.

## Velocidad 
Es la cantidad de trabajo que un equipo puede completar en un sprint. Se mide generalmente en puntos de historia, que representan el esfuerzo relativo de las tareas en función de su complejidad y tamaño.

Cantidad de **puntos de historia** que el equipo completa por Sprint.

## Metricas
### Burndown Chart

![Screenshot 2025-03-25 143133](https://github.com/user-attachments/assets/a7b8c3ce-a9d6-4f29-b357-2333711b751e)

### Epic Burndown
Es una variación del Burndown Chart, pero en lugar de enfocarse en un sprint, se utiliza para hacer seguimiento del progreso de una épica (una gran funcionalidad o conjunto de historias de usuario relacionadas) a lo largo de múltiples sprints.

![image](https://github.com/user-attachments/assets/4dcda054-fd65-429b-9a42-1edf2c03038d)

### Velocity Chart
Para visualizar la cantidad de trabajo completado por un equipo en cada sprint. Se usa para medir la velocidad del equipo.

![image](https://github.com/user-attachments/assets/952f46bd-38e4-4862-ad9f-eb007b335cd8)

<div style="page-break-after: always;"></div>

# Product Discovery
Es un disciplina que nos ayuda a construir mejores productos.

El Product Discovery es la fase del desarrollo de un producto en la que se exploran, validan y definen las necesidades del usuario y las oportunidades de mercado antes de empezar a construirlo. Su objetivo es asegurarse de que el producto que se va a desarrollar realmente resuelve un problema y aporta valor a los usuarios.

## MVP Minimo producto viable
Es la versión más simple de un producto que permite validar su idea con el menor esfuerzo posible. La clave es desarrollar solo las funcionalidades esenciales para probar si realmente resuelve un problema y tiene valor para los usuarios.

Es un producto barato, simple que lleva horas o dias en desarrollar. Solo para ver que onda.
![image](https://github.com/user-attachments/assets/709d3939-c16a-41bd-94ee-be48a884a794)

Si el MVP tiene éxito, se puede expandir el producto con más funcionalidades. Si no, se pueden hacer ajustes basados en la retroalimentación.

## Relacion entre ambos
>**El MVP es una forma de validar hipótesis del Product Discovery**

Ambos minimizan el riesgo de construir algo inútil
- Product Discovery evita desarrollar productos basados solo en suposiciones.
- El MVP permite probar rápidamente si la solución funciona antes de invertir más recursos.

El producto final es aquel que queda despues de que "muere" el producto, es la ultima version que ya no sirve. 
Un producto es una constante evolucion de si misma, que empezo en el MVP.

### Prueba de concepto
Es un experimento o demostración a pequeña escala que se realiza para verificar si una idea, tecnología o solución es factible antes de invertir recursos en su desarrollo completo.
![image](https://github.com/user-attachments/assets/9e331720-fcb5-47e6-95fe-5daccef34f3b)
Se "practica" hasta que se llega a un producto estable.

### Discovery, no solo al inicio (Dual Track)
En lugar de que el Discovery sea solo una fase inicial. Esto significa que el equipo de producto está constantemente explorando nuevas ideas y mejorando el producto mientras lo desarrolla.
![image](https://github.com/user-attachments/assets/f79d45df-01d6-4b19-84d7-4540eebb9793)

## Mentalidad de Product Discovery
![image](https://github.com/user-attachments/assets/a0aa2ffb-d9e1-463e-a7d1-0d335314b569)
1. Colaboracion y aprendizaje en el equipo de producto: todo el Equipo de Producto conoce y aprende del Product Discovery, participando en las decisiones sobre la funcionalidad a crear.
2. User Centered Design: el Equipo de Producto trabaja en comunicacion directa con usuarios y clientes. No solo validadndo problemas y soluciones sino ademas co-creando junto a ellos
3. Humildad intelectual: se necesita tolerancia a la incertidumbre: no hay certezas sino hipotesis a validad; un ambiente seguro e inclusivo. Experimentos: tolerancia al error y a cambiar de parecer

## Problema vs Solucion
![image](https://github.com/user-attachments/assets/fe399cf8-2b91-483e-a83f-9bd82075a95a)
Por ahi se apunta a resolver un problema que en realidad no era un problema. Algo que no resolvia o que no es importante para los usuarios.

## Entrega de valor
 **Colaboramos para Entregar Valor**
 
 **Reflexionamos para Mejorar**
 
![image](https://github.com/user-attachments/assets/ab8fa578-dbe1-476e-8259-2ed2e59040ae)

## Personas (UX Personas)
Es una tecnica para hacer **foco en segmentos especificos**. Para comprender las diferentes necesidades de los principales **tipos de clientes** de un producto. Una UX Persona es un personaje ficticio que representa a tus usuarios objetivo. 

Las personas son representaciones de un grupo de usuarios con comportamientos, objetivos y motivaciones similares.

La puesta en marcha de esta técnica puede ser útil tanto para la estrategia como en la toma de decisiones de diseño. Uno de sus principales beneficios es que permite a los miembros del equipo identificar y conocer a los usuarios.

![image](https://github.com/user-attachments/assets/d36c5346-cbf4-4061-a413-b32241fcfb49)

## Mapa de Empatia
Es una herramienta visual que ayuda a comprender mejor a los usuarios o clientes al profundizar en sus pensamientos, emociones, necesidades y comportamientos.
![image](https://github.com/user-attachments/assets/9ecdd020-2624-4295-8e99-63e9c7d09d48)
![image](https://github.com/user-attachments/assets/2273368e-9144-4948-81fa-9bb0301b5a80)

<div style="page-break-after: always;"></div>

# Historias de Usuario

Esta tecnica esta asociada a las metodologias agiles.

Es una descripcion de la funcionalidad del sistema, desde el punto de vista de un usuario:
- **Como** [persona]
- **quiero** [tal funcion]
- **para** [este objetivo]

Se enocan en dar valor. Algo util, para definir qué necesita hacer el sistema y por qué.

## Como escribir historias de usuario de calidad

### Framework QUS (Quality User Story)
- Calidad **sintactica**: con el formato correcto, minimas, atomicas.
- Calidad **semantica**: que use bien los conceptos del dominio sobre el que se trabaja, sin ambiguedades, orientadas al problema no a la solucion, sin conflictos entre historias
- Calidad **pragmatica**: unicas entre si, uniformes, independientes entre si, completas.

###  Criterios INVEST
Se recomienda que las tareas del backlog cumplan:
- Independiente (no depende de otra historia)
- Negociable (se puede ajustar según necesidad)
- Valiosa (aporta valor al usuario)
- Estimable (puede medirse el esfuerzo para desarrollarla)
- Small (pequeña, fácil de implementar, desarrollable en una iteracion)
- Testable (se puede verificar que está bien hecha)

## -
**Epicas**: historias de usuario que se pueden descomponer en mas historias de usuario. Deseamos subdividir las epicas hasta llegar a tareas de tamanio razonable


## 3 Cs (Card, Conversation, Confirmation)
-**Card**: describe la intencion del usuario <br/>
-**Conversacion**: los interesados sse comunicn olara refinar las historias, descubriendo y documentando requisitos. <br/>
-**Confirmacion**: criterios de aceptacion; listado de items para que tal historia de usuario se considere terminada.<br/>

### Criterios de Aceptacion
Condiciones especificas que deben cumplirse para aceptar el trabajo realizado: listas de condiciones, escenarios

Se usa el formato
- Dado que [contexto]
- cuando suceda [evento]
- entonces [consecuencia]

Similar a las historias de usuario, deben tener claridad, deben ser concisos, verificables, independientes y orientados al problema.

##  Behaviour Driven Development
Orientado al comportamiento. Es una metodología que extiende TDD (Test-Driven Development), para definir cómo debe comportarse el sistema antes de implementarlo.

Proceso iterativo: se empieza por las historias de usuario

![image](https://github.com/user-attachments/assets/4c37e72b-859a-4cf7-8000-a9df5e6c8206)

![image](https://github.com/user-attachments/assets/1e952861-ce54-4899-a5e9-d04939d679cb)

Herramienta: <https://cucumber.io/>

### Casos de uso
Los casos de uso describen cómo un sistema interactúa con los usuarios u otros sistemas para lograr un objetivo. Son más detallados que las historias de usuario y ayudan a definir el flujo de trabajo dentro del sistema.
Descripcion de:
- serie de acciones
- realizadas por un sistema
- que generan un resultado observabe de valor para un actor partcular

Compuestos de un escenario principal y un conjunto de escenarios alternativos.

En UML
![image](https://github.com/user-attachments/assets/e4757061-a52a-4125-967d-400ff11a4f98)

## Como encontrar historias
- Establecer los limites del sistema
- Identificar actores involucrados en el sistema
- Buscar objetivos y actividades dentro del sistema. Herramientas: User story mapping, impact mapping

### User Story Mapping
Ayuda a definir el producto a desarrollar. Queda un diagrama donde todo esta agrupado por grupos funcionales

![image](https://github.com/user-attachments/assets/79dc335a-8fa9-4119-9f89-135a86393a99)

1. Nivel superior (rojo) → Representa las grandes actividades o funcionalidades principales del sistema.
2. Segundo nivel (amarillo) → Son las subactividades o pasos dentro de cada funcionalidad.
3. Tercer nivel (azul) → Son las tareas específicas que se implementan en diferentes versiones (v1, v2, v3).

### Impact Mapping
Orientada a los objetivos del negocio, para alinear objetivos de negocio con entregables del producto, asegurando que todo lo que se desarrolle tenga un propósito claro y valor real.
![image](https://github.com/user-attachments/assets/3913268b-4aa3-4df8-88f4-10449ebc6268)

- Objetivo → Qué se quiere lograr (ej: “Aumentar el uso de la app de recetas”)

- Actor → Quién está involucrado (usuarios, administradores, etc.)

- Impacto → Cambios esperados en el comportamiento de los actores

- Entregable → Qué funcionalidad o tarea concreta se desarrollará para provocar ese impacto

Ejemplo: Ann mira y se va, Dave compra solo los dias de oferta
![image](https://github.com/user-attachments/assets/353e7760-273e-41fd-815e-03461712580a)


<div style="page-break-after: always;"></div>

#  Modelo de Dominio

## Complejidad del Desarrollo de Software
Para resolver un problema es necesario entenderlo antes de empezar a pensar una solucion 
- **Complejidad** = `Complejidad Esencial + Complejidad Accidental`
- **Complejidad Esencial** = `Complejidad Problema + Complejidad Solucion`

### Mecanismos para atacar la complejidad (En objetos)
- Descomposicion -> Descubrir
- Abstraccion -> Pensar
- Establecer Jerarquias -> Inventar

Un modelo es una representacion simplificada de la realidad

Los modelos permiten:
- Visualizar
- Entender
- Especificar

Y siven de
- Guia
- Documentacion

El modelo de dominio es una representación conceptual del problema que se quiere resolver en un sistema de software. Básicamente, define los elementos principales del dominio (objetos, entidades, relaciones) y cómo interactúan entre sí.

El **modelo de dominio** se construye a partir de los casos de uso, que describen qué acciones pueden realizar los usuarios en el sistema. El modelo de dominio se divide en dos partes:
- Comportamiento: Representa la lógica del sistema, cómo los elementos interactúan. Diagramas de secuencia o diagramas de colaboración.
- Estructura: Representa la organización de las entidades del dominio y sus relaciones. Diagramas de clases.

Después, el **modelo de diseño** refina el modelo de dominio agregando detalles técnicos, para luego convertirlo en código.

![image](https://github.com/user-attachments/assets/84cf5646-d4cb-43df-a150-c1fe6a3da50a)

# Tecnicas
- Buscar sustantivos y verbos significativos en casos de uso, minutas, etc. Es como leer un enunciado y empeza a extraer.
- Cosas utiles a extraer son: actores, objetos fisicos, lugares, eventos, procesos.

## CRUD: Create, Read, Update, Delete
Toda entidad debe ser creada y leida en alguna funcionalidad. Usualmente, tambien pueden modificarse o eliminarse. Si falta una operacion, entonces falta una funcionalidad.
![image](https://github.com/user-attachments/assets/c1241319-fc5a-41ab-873c-10605dfda84d)

## Streamlined Object Modeling
Dentro de Streamlined Object Modeling, hay tres elementos clave:
- Patrones de Colaboración: Definen cómo interactúan los objetos.
- Reglas de Negocio: Restringen esas interacciones.
- Recetas de Implementación: Explican cómo programar esas reglas en el código.

### Patrones de Colaboracion 
Son estructuras comunes para organizar y modelar las interacciones dentro de un sistema. Se utilizan para representar cómo los diferentes elementos de un sistema trabajan juntos y cómo ocurren los eventos en un flujo de trabajo.

![image](https://github.com/user-attachments/assets/62a34b7a-561c-466c-b23f-936fbc80557d)

![image](https://github.com/user-attachments/assets/675f2f3d-f0bd-4d71-b878-d0a1e94db180)

#### Actor - Rol
  - Un actor puede conocer varios roles, pero solo puede tomar uno de cada tipo. Toda acción que tome será en contexto de un rol. Un actor (persona o sistema) puede tener diferentes roles, pero solo desempeña uno a la vez.
  - Ejemplo: Un usuario puede ser "Cocinero" o "Administrador", pero no ambos al mismo tiempo.
![adadawdw](https://github.com/user-attachments/assets/26bdf8a5-a6c1-4e1e-aa27-057746760ac6)

#### Gran Lugar - Lugar
  - Un lugar puede formar parte de un gran lugar más amplio. Un gran lugar sirve como contenedor de sus lugares.
  - Ejemplo: "Cocina" (gran lugar) tiene dentro una "Estación de trabajo" (lugar).
![image](https://github.com/user-attachments/assets/87d6f7f0-a51d-4ae3-bb40-9f34c4f41015)

#### Ítem - Ítem Específico
  - Un ítem general tiene variantes específicas. El ítem describe la información que es común en todas las variantes específicas
  - Ejemplo: "Receta de Pizza" (ítem) puede tener una versión "Pizza Margarita" y otra "Pizza Pepperoni" (ítems específicos).
![image](https://github.com/user-attachments/assets/b00f15d8-50e7-494b-9787-24aaf197dbf2)

#### Ensamble - Parte
  - Un ensamble está compuesto de partes.
  - Ejemplo: Una receta (ensamble) está formada por ingredientes (partes).
![image](https://github.com/user-attachments/assets/11f5ce10-781b-440f-9822-6f7ae5c0d4db)

#### Contenedor - Contenido
  - Un contenedor almacena elementos dentro de él.
  - Ejemplo: Un recetario (contenedor) almacena varias recetas (contenido).
![image](https://github.com/user-attachments/assets/bfdac1e2-7701-4da7-81a6-631bb9e05cca)

#### Grupo - Miembro
  - Un grupo está formado por miembros. Los grupos modelan colecciones y clasificaciones de cosas, personas y lugares
  - Ejemplo: Un "Grupo de Cocineros" tiene miembros que son usuarios interesados en compartir recetas.
![image](https://github.com/user-attachments/assets/569943dc-08fe-4dea-92c7-8bdddadf3b7b)

Las multiplicidades (por ejemplo, "uno a muchos" o "muchos a muchos") ayudan a diferenciar relaciones similares como Grupo-Miembro, Contenedor-Contenido y Ensamble-Parte.

#### Patrones de Transaccion Simple
Modelan acciones individuales dentro del sistema. Una transaccion conoce:
- Quién la realiza (ejemplo: un usuario).
- Dónde se realiza (ejemplo: en la sección de recetas).
- Sobre qué se actúa (ejemplo: una receta específica).
![image](https://github.com/user-attachments/assets/182b7f5f-f9b0-4899-be94-3bad20a5a9ca)

#### Patrones de Transaccion Compuesta
Describen interacciones más complejas que involucran múltiples pasos o actores en un sistema
![image](https://github.com/user-attachments/assets/a6817823-e261-43a7-95dc-87772e08d36a)

#### Transaccion - Transaccion Cronologica
Usa el patrón de transacciones encadenadas donde una acción sigue a otra anterior. Este patrón modela procesos secuenciales, donde cada paso depende del anterior.
- Ejemplo:
1. Un usuario compra ingredientes en línea.
2. Luego recibe una confirmación de compra.
3. Finalmente, se envía el pedido a su casa

![image](https://github.com/user-attachments/assets/8ff94dc2-f1dd-4076-a2b1-4807655d82e5)

### Reglas de Negocio
Restricciones que gobiernan las acciones dentro de un dominio de negocio. Las reglas de negocio son restricciones que determinan cómo pueden interactuar los objetos dentro de un sistema. Estas reglas aseguran que el sistema funcione correctamente y refleje la realidad del negocio.

En SOM, las reglas de negocio se convierten en reglas de colaboración. Esto significa que antes de modificar las relaciones entre los objetos, el sistema debe verificar que se cumplan ciertas restricciones.

Donde ubicarlas?
- Si no se ubican en el modelo, el mismo es incompleto. La dinamica de objetos sera externa a ellos
-  Deben estar en el objeto que tenga más información relevante.

### Reglas de Negocio
Tipos de reglas:
- Tipo: un medicamento puede ser cargado solo en un container refrigerado
- Multiplicidad: un pallet refrigerado puede contener hasta 10 cajas
- Propiedad: un pago debe registrar un numero valido de tarjeta de credito
- Estado: una orden no debe sert entregada si antes fue cancelada
- Conflicto: un vuelo no puede ser programado en una puerta en un mismo horario que otro vuelo

<div style="page-break-after: always;"></div>

# Diagramas UML

UML formaliza como representar ciertos aspectos del software en diagramas. Se usan aproximaciones al formalismo.

![image](https://github.com/user-attachments/assets/da76dd75-6804-4fb3-ad81-ea16de37c8a5)

## Diagrama de Estructura

### Diagrama de objetos
Representa instancias concretas de clases en un momento específico del tiempo para ver los objetos del sistema y como se interrelacionan.

### Diagrama de paquetes
Diagrama por encima del diagrama de clases. Su objetivo es organizar y agrupar los elementos del sistema (como clases, interfaces o incluso otros paquetes) para mostrar la estructura modular de alto nivel del software.

Muestra la organización y disposición de diversos elementos de un modelo en forma de paquetes.

![image](https://github.com/user-attachments/assets/079791bf-a25c-4753-acc5-c13de1fa6801)

### Diagrama de componentes
Muestra cómo se estructura el software en componentes independientes y cómo estos se conectan entre sí.

1. Componentes:
    -Se representan con un rectángulo con el ícono de un componente (pequeño rectángulo con dos salientes).
2. Interfaces:
    - Se representan como círculos (interfaces proporcionadas) o semicírculos (interfaces requeridas).
    - Conectan componentes entre sí.
3. Dependencias:
    - Flechas que indican que un componente depende de otro para funcionar.


### Diagrama de despliegue
Se usa para mostrar cómo se distribuyen los componentes del sistema en el hardware, es decir, dónde y cómo se ejecutan. Modela la disposicion fisica de los artefactos sofware en nodos.

Muestra cómo se asignan los artefactos de software a los componentes de hardware, conocidos como nodos, e ilustra las configuraciones físicas de software y hardware que son críticas para la ejecución, operación y escalabilidad de un sistema. 

![image](https://github.com/user-attachments/assets/68ac6695-8ddb-4b84-a65e-104d407ac8b0)

- Nodos
  - Los nodos a menudo se representan como un cubo y representan los elementos físicos de un sistema, como servidores o dispositivos.

- Artefactos
  - Los artefactos son los elementos tangibles, como programas de software o archivos, que viven en los nodos.

- Relaciones
  - Las relaciones ilustran cómo los artefactos están conectados y cómo se comunican a través del sistema.

### Diagrama de perfil
**Estereotipo** -> Mecanismo de extension, extiende un elemento UML (como clase, componente, nodo...). Aplicado a un elemento de cualquier otro diagrama, modifica como se interpreta. Se representa como una clase con la palabra <<stereotype>>.

El diagrama de perfil es básicamente un mecanismo de extensibilidad que le permite ampliar y personalizar UML agregando nuevos bloques de construcción, creando nuevas propiedades y especificando nueva semántica para hacer que el lenguaje sea adecuado para su dominio de problema específico. 

Un pefil UML formaliza un conjunto de esterotipos, tags y restricciones que se pueden aplicar a otros diagramas.

**Metaclass** -> Elementos donde. Son clases UML que se extienden, como `Class`, `Component`, `Node`, etc.

![image](https://github.com/user-attachments/assets/84e16b6b-a7af-4a5b-b12b-660d61290b2c)

## Diagrama en Comportamiento

### Diagrama de actividad
Para modelar procesos de negocio o algoritmos. Para representar casos de uso de forma detallada.

**Componentes**:
- Circulo negro: ahi empieza <br/>
- Circulo negro con reborde blanco: ahi termina <br/>
- Rectángulo con bordes redondeadosL: representa una acción o tarea.
- Hexagono: chequeo, bifurca el flujo según condiciones.
- Flechas que conectan los elementos y muestran el orden.
- Línea gruesa horizontal o vertical: _fork_/_join_; indican que varias actividades comienzan o terminan en paralelo. Desde la linea salen varias flechas hacia actividades que se ejecutan en paralelo. El join también se muestra como una línea gruesa, pero aquí varias flechas entran y una sola sale, indicando que el flujo espera que todas las actividades anteriores terminen antes de continuar

![image](https://github.com/user-attachments/assets/91191e4e-1054-46f9-81f9-1d75ddcd5e21)

### Diagrama de casos de uso
Se utiliza para representar las funcionalidades principales de un sistema desde el punto de vista del usuario, sin entrar en detalles técnicos.

### Diagrama de maquina de estados
Sirve para representar el comportamiento de un objeto o sistema en función de sus estados y cómo cambia de estado ante ciertos eventos.

Para modelar comportamientos dinámicos de un sistema. Para objetos que cambian de estado dependiendo de eventos o condiciones.
**Componentes**:
- Rectángulo redondeado: estado
- Círculo negro: representa el punto de partida.
- Círculo con un contorno: fin del proceso.
- Flechas entre estados: transciones
![image](https://github.com/user-attachments/assets/1b1d66ec-450b-4433-af0e-2a108dd71e8a)

![image](https://github.com/user-attachments/assets/f4d2ffbf-2b59-4245-bc1b-7b043e68b91e)

### Diagrama de secuencia 
Modela la interacción entre objetos o componentes a lo largo del tiempo
Para ver quién le habla a quién, cuándo y en qué orden.

![image](https://github.com/user-attachments/assets/f25d1da0-2ada-46c4-ac8e-6f6393dbf886)


### Diagrama de comunicacion
Es un diagrama de interacción que muestra información similar a los diagramas de secuencia pero su foco principal es en la relación de objetos.

Muestra cómo se comunican los objetos entre sí, enfocándose más en la estructura de las relaciones que en el tiempo.

Los objetos se colocan como nodos en el espacio, y se conectan con líneas que representan los mensajes.

> La diferencia entre el de secuencia y el de comunicacion es que uno resalta quién se comunica con quién (comunicación) y el otro cuándo ocurre cada mensaje (secuencia).

### Diagrama de tiempos
Se usa para mostrar cómo cambian los valores o estados de uno o más objetos a lo largo del tiempo. Muestra cómo evolucionan variables o eventos a lo largo del tiempo.

![image](https://github.com/user-attachments/assets/fe6b2e6b-cd59-40d2-aed0-2dbb3a1c45a2)



<div style="page-break-after: always;"></div>

# Atributos de Calidad

Un atributo de calidad es una medida o propiedad testeable de un sistema que es usada para indidcar como el sistema satisface las necesidades que se le pide cumplir.

## Clasificacion 

### Internos/externos y Operacional/No-Operacional
- **Internos**: aquellos atributos de calidad que pueden ser evaluados sin ejecutar el sistema. Se basan en el análisis del código, la arquitectura o los documentos del sistema
- **Externos**: solo pueden ser evaluados cuando el sistema está en ejecución. Se relacionan directamente con la experiencia del usuario o con el comportamiento observable del sistema
- **Operacionales**: son aquellos atributos que afectan directamente al uso diario del sistema. Es decir, definen el comportamiento del sistema durante su operación normal
- **No-Operacionales**: tienen que ver con el proceso de desarrollo y mantenimiento del sistema más que con su uso directo

![image](https://github.com/user-attachments/assets/17e98c89-26b7-4d50-ae67-977eb40a5ad5)

### Norma ISO/IEC FCD 25010
Es otro tipo de clasificacion posible. Propone un conjunto de atributos que se va mirar en un sistema <ins>para definir la calidad del sistema</ins>.
![image](https://github.com/user-attachments/assets/59eddd3a-184d-4128-8c81-028ecfe94c6d)

## ¿Por que se rediseñan los sistemas?
Se decide rediseñar por cuestionen funcionales, porque es de poca calidad (mala performance, poco escalable, problemas de seguridad, etc) o sea que viola atributos de calidad. 

![image](https://github.com/user-attachments/assets/9d6adca0-3873-4d1e-be7b-73b11eed7823)

Deben ser considerados a los largo de todo el ciclo de vida del sofware para tener exito.

No dependen solamente de la etapa de diseño, no dependen solamente de la implementacion o entrega.

![image](https://github.com/user-attachments/assets/171efea4-17b2-478d-8e20-2dd6fa9faf8f)

Pueden entrar en conflicto con otros:
- seguridad vs confiabilidada: si no es seguro no va a ser confiable
- portabilidad vs performance: si tiene mala performance seguro sea poco portable
- seguridad vs usabilidad
- etc

El objetivo es evaluar segun el sistema en cuestion: consensuar una priorizacion de los atributos de calidad y diseñar un sistema lo suficientemente bueno para todos los interesados.

## Atributos

### Disponibilidad - Availability

> ¿Qué haría fallar al sistema? <br>
¿Qué tan probable es que ocurra? <br>
¿Cuánto tiempo lleva repararlo?
 
Es un atributo de calidad que se refiere a la capacidad del sistema para estar en funcionamiento y accesible cuando se lo necesita. Se trata de la capacidad de un sistema de estar disponible y operativo durante un periodo de tiempo especificado. Es que tan disponible puede estar un sistema.

#### Aspectos clave de la disponibilidad
<ins>Medición de la Disponibilidad</ins>: La disponibilidad se mide generalmente en términos de un porcentaje, que representa la proporción de tiempo en el que el sistema está operativo en relación con el tiempo total.

<ins>Factores Clave</ins>: La disponibilidad del software se ve influenciada por varios
factores como: diseño robusto, gestión de recursos, mantenimiento y actualizaciones, recuperación ante desastres.

La disponibilidad es esencial para garantizar que los sistemas de software cumplan con las expectativas de usuarios y necesidades del negocio. Se debe buscar implementar estrategias para mitigar fallos y garantizar la continuidad del servicio como balanceo de carga, replicacion de datos, respaldo y recuperacion, escalabilidad.

### Performance
Corresponde a los tiempos de respuesta de la aplicación en relación a las funcionalidades o actividades soportadas por la misma.

Para medir la performance de un sistema se consideran la
- Latencia: Tiempo dedicado a responder a un evento.
- Capacidad: El número de eventos que pueden ocurrir en un tiempo determinado.

### Interoperabilidad
Interoperabilidad es un atributo que mide la capacidad de intercambio de información de la aplicación con otros sistemas.

Una aplicación bien diseñada facilita la integración con otros sistemas.

Para mejorar la interoperabilidad, es conveniente utilizar interfaces externas bien diseñadas, normas de intercambio y estándares, entre otras

### Usabilidad
Se cumple la usabilidad cuando se respetan la 
- Comprensibilidad: que tan fácil es para el usuario comprender el sistema, que conocimientos previos requiere el usuario para poder trabajar con el software
- Facil uso/eficiente: que permita realizar las operación de manera rápida y efectiva
- Facil de recordar/Intuitiva/Estandar
- Atractiva/Agradable/Comoda: tiene que ver con el diseño 

### Seguridad
Es el atributo que permite medir la vulnerabilidad de las aplicaciones a ataques, versus la posibilidad de defensa del sistema ante pérdidas o robo de información estratégica y valiosa para la organización

Estos ataques pueden ser tanto externos como internos.

Se deben considerar:
- Capacidad de detección de ataques de denegación de servicio (DDoS), y respuesta ante éstos.
- Restricciones de acceso de usuarios de acuerdo a las políticas de autenticación y autorización.
- Prevención de la inyección de consultas SQL
- Encriptación de claves, contenidos y datos empresariales.
- Conexión segura

### Escalabilidad
Es la capacidad de manejar la carga de trabajo de la aplicación sin afectar el rendimiento de la misma, es la posibilidad de crecimiento sin perjudicar su funcionamiento operativo.

<ins>Como mejorar la escalabilidad</ins>:
- Vertical: Para crecer, se agregan más recursos físicos a la infraestructura que soporta al aplicativo, tales como memoria, almacenamiento en disco, procesador o capacidad de cómputo, ancho de banda, entre otras, para un aplicativo.
- Horizontal: Se incrementa el número de computadores para dividir la carga de trabajo de la aplicación.

<ins>Como medir la escalabilidad</ins>:
- Ver si el sistema permite el escalamiento vertical o distribución de la carga.
- El tiempo necesario para aumentar el escalamiento.
- Las limitaciones de escalamiento en la infraestructura operativa: número de servidores máximo, memoria, discos, o capacidades de la red.
- Posibilidades de escalamiento: incremento en el número de transacciones o carga de trabajo.


<div style="page-break-after: always;"></div>

# Modelo de Vistas de Arquitectura 4+1 

## ¿Qué es la arquitectura de un sistema?

Arquitectura: Son las partes de las que se compone el sistema y como se interconectan.

La arquitectura de un sistema no solo se trata de sus componentes, sino también de cómo están conectados y de las decisiones que se tomaron (y se tomarán) para construirlo y hacerlo evolucionar.

>La arquitectura de software son aquellas decisiones que son importantes y difíciles de cambiar

La arquitectura de software es
 - la forma del sistema
 - decisiones significativas de diseño
 - definido por el costo de cambiar algo
 - la division del sistema en componentes
 - comunicacion entre componentes

## ¿Cómo describimos la arquitectura de un sistema?
#### ¿A quién está dirigido un Documento de Arquitectura?
Dentro de un equipo de trabajo hay distintos roles (arquitectos, analistas, product designers, UX Researcher, UI Designer, UX Writer, scrum masters) a los que les van a interesar cosas distintas

Existen muchos interesados o stakeholders de un documento de arquitectura, e incluso estos pueden tener distintos intereses y conocimientos.

Se busca un **unico** documento o diagrama que pueda explicar la arquitectura.

### Modelo de vistas 4+1 - Kruchten
Se parte la arquitectura en 4 vistas

![image](https://github.com/user-attachments/assets/a254ea3f-7fdb-40c3-9297-63db96fe7daa)

Permite a través de diferentes vistas analizar distintas perspectivas del problema, focalizándose en el problema en cuestión. 

Concentra en un único documento las principales decisiones tomadas sobre el sistema. Permite a nuevos integrantes del equipo entender la arquitectura del sistema y ubicarse dentro de la solución

Ademas, permite discutir con todos los stakeholders las distintas decisiones y validarlas en una etapa temprana

#### Vista logica 
Muestra cómo está estructurado el sistema desde el punto de vista lógico, es decir, cómo se organizan sus componentes y clases para cumplir con las funcionalidades que el sistema debe ofrecer a los usuarios.

Se enfoca principalmente en los requisitos funcionales, o sea, en lo que el sistema tiene que hacer. Para diseñarla se utilizan conceptos como abstracción, encapsulamiento y herencia, típicos de la programación orientada a objetos.

Ayuda a entender mejor qué hace cada parte y también permite identificar patrones y soluciones comunes que pueden reutilizarse en distintos lugares del sistema.

Le interesa a los desarrolladores

#### Vista de procesos
Esta vista se encarga de mostrar cómo el sistema maneja aspectos como el rendimiento, la disponibilidad y la concurrencia, que son requisitos no funcionales. Es decir, no se trata de lo que el sistema hace, sino de cómo lo hace en términos de eficiencia y estabilidad.

Se centra en cómo se ejecutan las distintas tareas al mismo tiempo, cómo se distribuyen entre diferentes partes del sistema, y cómo se asegura que todo funcione bien incluso si hay fallos.

Un proceso es una agrupación de tareas que forman una unidad ejecutable. Los procesos representan el nivel al que la arquitectura de procesos puede ser controlada tácticamente.

#### Vista de desarrollo (o de componentes)
Tiene que ver con componentes. Un componente se refiere a un conjunto de cosas logicas que se empaquetan en un entregrable (un .exe por ej) 

Esta vista muestra cómo está organizado el software desde el punto de vista de los desarrolladores, es decir, cómo se estructura el código dentro del entorno de desarrollo.

El sistema se divide en módulos más pequeños, como bibliotecas o subsistemas, que pueden ser creados y mantenidos por uno o varios desarrolladores

Esta vista considera aspectos como la facilidad para desarrollar y mantener el software, la posibilidad de reutilizar componentes, y también las limitaciones propias del lenguaje de programación o de las herramientas que se estén usando.

Se trata de cómo organizar el software para que sea más fácil de construir, entender y mantener.

#### Vista fisica (o de despliegue)
Como despliego el sistema. Toma en cuenta primeramente los requisitos no funcionales del sistema tales como la disponibilidad, confiabilidad (tolerancia a fallas), rendimiento (throughput), y escalabilidad. 

Se enfoca en cómo se distribuye físicamente el sistema, es decir, cómo se instala y ejecuta el software en los distintos servidores, computadoras o nodos de red.

Se espera que el sistema pueda tener diferentes configuraciones: una para desarrollo, otra para pruebas y otras para entornos reales con distintos usuarios. Por eso, esta vista busca que la relación entre el software y los equipos donde se ejecuta sea flexible y fácil de adaptar, sin que eso implique tener que cambiar el código fuente.

#### Vista de escenarios 
Los elementos de las cuatro vistas trabajan conjuntamente en forma natural mediante el uso de un conjunto pequeño de escenarios relevantes. Los escenarios son los casos de uso del sistema. 

Sirve a dos propósitos principales:
- Como una guía para descubrir elementos arquitectónicos durante el diseño de arquitectura
- Como un rol de validación e ilustración después de completar el diseño de arquitectura, o sea ver si el sistema cumple con los casos de uso planteados.


<div style="page-break-after: always;"></div>

# Patrones de arquitectura de software

## Layers
El patrón de arquitectura por capas organiza el sistema dividiéndolo en distintos niveles, donde cada capa tiene una responsabilidad específica y se comunica solo con la capa inmediatamente inferior o superior.

Cada capa actúa como un filtro o intermediario, permitiendo que los cambios en una parte del sistema no afecten directamente a las demás.

<img src="https://github.com/user-attachments/assets/75d254b5-a6a9-4eda-a44a-3a84ce18202e" width="400"/>
<img src="https://github.com/user-attachments/assets/bb2d3e6d-41a9-4bfe-bdc7-4cdfad928649" width="200"/>

- Capa de presentación: aca va todo lo que es presentacion de datos al usuario.
- Capa de negocio: todo lo que tiene que ver con casos de uso.
- Capa de acceso a datos: leer y escribir información desde y hacia la base de datos u otras fuentes.

## Broker
La idea principal es tener un intermediario (el broker) que se encarga de coordinar la comunicación entre los distintos elementos del sistema.

Ej: el servidor 1 le quiere mandar un mensaje al servidor 2: el servidor 1 le manda el mensaje al broker, el broker se lo despacha al servidor 2.

Los componentes no necesitan saber nada sobre la ubicación o los detalles de implementación de los otros, lo que mejora el desacoplamiento y la escalabilidad.

<img src="https://github.com/user-attachments/assets/5147e1ba-695b-4432-8350-77b111cd969e" width="400"/>

## Pipe & Filters
Propone un modelo donde hay un conjunto de datos que fluye de un lado a otro donde, en el camino va sufriendo ciertas transformaciones. 

La idea es dividir una tarea compleja en una serie de filtros, donde cada uno realiza una operación específica, y conectarlos entre sí mediante tuberías (pipes) que transportan los datos de un filtro al siguiente.

Cada filtro funciona como un módulo independiente: recibe una entrada, la procesa y entrega una salida que se convierte en la entrada del siguiente filtro.

<img src="https://github.com/user-attachments/assets/e517eb4d-5962-456b-b0a8-bab58bce6327" width="400"/>

## Hexagonal Architecture (Ports & Adapters)
Propone una forma de diseñar sistemas en la que se separa completamente el núcleo de la aplicación (la lógica de negocio: los casos de uso del sistema) del mundo exterior (como interfaces de usuario, bases de datos, redes, etc.). El objetivo es que el corazón del sistema no dependa de detalles técnicos externos.

<img src="https://github.com/user-attachments/assets/3bf3ae87-34fb-4a77-ae99-5edf288c5259" width="400"/>

### Domain Layer
Representa el corazón del sistema. Es donde se modelan las reglas del negocio, los conceptos principales del problema que se está resolviendo y la lógica que gobierna el comportamiento del sistema.

![image](https://github.com/user-attachments/assets/3057516f-96e1-400c-b655-f59c8db4acb8)

### Application Layer
Es la encargada de orquestar la lógica del sistema. Su función principal es coordinar el flujo de trabajo entre los componentes del sistema.

Esta capa no contiene reglas de negocio como tal, pero sabe cómo usarlas

![image](https://github.com/user-attachments/assets/df25bd25-1b94-43ea-96a3-ca6c0fc8fc12)

### Infrastructure Layer
Su responsabilidad principal es conectar el mundo externo con el sistema.

![image](https://github.com/user-attachments/assets/4df9b7e7-a1cb-42d2-97d3-b256d0438235)

### Principio de Inversión de Dependencias
En un sistema, se puede tener una capa de lógica de negocio (módulo de alto nivel) y una clase que se conecta a una base de datos (módulo de bajo nivel). De manera natural, el módulo de alto nivel utilizaría directamente el módulo de bajo nivel. Sin embargo, al hacer esto, la lógica de negocio queda atada a una implementación concreta, lo que limita la flexibilidad del sistema.

Con el Principio de Inversión de Dependencias (DIP), lo que se busca es invertir la dirección de las dependencias. En lugar de que la lógica de negocio dependa directamente de la implementación de la base de datos, se define una interfaz o abstracción. La clase concreta que maneja la base de datos (o cualquier otro detalle técnico) será la que implemente esta interfaz. De esta manera, el módulo de negocio solo depende de una abstracción, sin preocuparse por los detalles de la implementación específica que se encuentre detrás de dicha interfaz.

### Despues de la Hexagonal Architecture
![image](https://github.com/user-attachments/assets/40e24523-8ee9-4caa-9818-3edc17762f13)

## Microservicios
Los microservicios son una arquitectura de software que consiste en descomponer una aplicación monolítica en un conjunto de servicios pequeños, autónomos y desarrollados de manera independiente. Cada servicio tiene una responsabilidad específica y se comunica con otros servicios a través de interfaces bien definidas, usualmente utilizando protocolos ligeros como HTTP o mensajería asincrónica.

Se agrega una complejidad tecnica.

![image](https://github.com/user-attachments/assets/12e66c7d-2134-43e2-9a57-38a98aadc5f9)


## Micro Frontends

El enfoque de Micro Frontends extiende los principios de la arquitectura de microservicios al desarrollo del frontend.

Cada micro frontend representa una funcionalidad o sección autónoma del frontend.

![image](https://github.com/user-attachments/assets/b6c840aa-100b-49cf-ab87-2ee4e5ddfc59)

<div style="page-break-after: always;"></div>

# RESTful API
- Significa **Re**presentational **S**tate **T**ransfer
- Utiliza estandares existentes como HTTP
- Comunicacion cliente-servidor
- Se presenta en 3 niveles de madurez
- Es un estilo de arquitectura para diseñar servicios web

## Caracteristicas
- Arquitectura cliente-servidor

- Stateless: cada request se ejecuta de forma independiente del resto. No guarda contexto. El servidor no guarda estado entre una petición y otra. Esto hace que las APIs REST sean más escalables y fáciles de mantener. Cada request contiene toda la informacion necesaria para completarse.

- Cacheable: Las respuestas pueden ser almacenadas (cacheadas) por el cliente o intermediarios. Reduce ancho de banda usado, reduce latencia y carga en servidores.<br>
  La cacheabilidad es la capacidad de estos sistemas para etiquetar de alguna forma las respuestas para que otros mecanismos intermedios funcionen como un caché. Estos sistemas o mecanismos intermedios (existen entre el cliente y el servidor) deben ser por lo general transparentes para los desarrolladores, no deben afectar la manera en que los servicios se consumen.

- Compresion: las APIs suelen retornar representaciones en varios formatos y estos formatos XML, HTML, JSON, etc, pueden ser comprimidos para ahorrar ancho de banda sobre la red

- Expone recursos (URI: Uniform Resource Identifier): Cada recurso en una API REST se identifica de forma única mediante una URI, identifica los recursos por clase o tipo. Hay una distincion de recursos principales y subordinados.

- Usa explicitamente los verbos HTTP:
  - **GET**: solicita una representacion de un recurso especifico
  - **POST**: enviar una entidad a un recurso en especifico
  - **DELETE**: borra un recurso en especifico
  - **PUT**: reemplaza todas las representaciones actuales del rescurso de destino con la carga util de la peticion. Pisa el recurso viejo con el recurso nuevo
  - **PATCH**: aplica modificaciones parciales a un recurso (a diferencia del PUT que pisa todo)
  - **OPTIONS**: para preguntar que puede hacer. Describe las opciones de comunicacion para el recurso de destino.<br>
  Ademas esta el uso de HTTP Status Codes:
![image](https://github.com/user-attachments/assets/151b69d3-c41e-476c-90a9-d7d2b5e55b10)

- Navegable

## Security Design Principles
| Principio / Recomendación                          | Descripción                                                                                             |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **Least Privilege**                                | Tener el menor privilegio requerido para realizar las acciones.                                         |
| **Fail-Safe Defaults**                             | Por defecto, no se debe tener acceso a los recursos.                                                    |
| **Complete Mediation**                             | El sistema debe validar los permisos de acceso a todos los recursos.                                    |
| **Keep it Simple**                                 | Mantener el diseño y la lógica de seguridad lo más simple posible.                                      |
| **Password Hashes**                                | Nunca guardar contraseñas en texto plano; siempre usar algoritmos de hash seguros.                      |
| **Never expose information on URLs**               | No exponer usernames, contraseñas, API keys ni información sensible en la URL.                          |
| **Timestamps en los requests**                     | Considerar agregar marcas de tiempo para detectar o prevenir ataques de repetición (replay attacks).    |
| **Validación de parámetros de entrada**            | Validar siempre los datos recibidos, para evitar inyecciones y otros tipos de ataque.                   |
| **Monitorear transacciones sospechosas**           | Detectar patrones inusuales (como muchas peticiones por IP), limitar la velocidad o aplicar delays.     |

### Monitoreo de transacciones sospechosas
- Control de cantidad de resquests por IP o por token/JWT/user para evitar problemas de DDoS, o para evitar/controlar el uso excesivo que puede bajar la performance de la API
- Limitacion de velocidad, o de tiempos de demora entre una request y otra para ciertos casos, ayuda a reducir la solicitudes excesivas que relantizarian la API
- APIs pagas como las de google por ej. permiten configurar limites de uso, tarifa, para evitar un mal uso o bug que genere por error multiples llamadas a la API

## Autenticacion y Autorizacion

**Autenticacion**: Es el proceso de verificar quién sos. En otras palabras, el sistema necesita confirmar tu identidad

**Autorizacion**: Es el proceso de verificar qué estás autorizado a hacer. Una vez que el sistema sabe quién sos, determina qué acciones tenés permiso para realizar o qué recursos podés acceder.

### Basic Auth
Basic Authentication es un método simple donde el cliente envía su nombre de usuario y contraseña codificados en Base64 dentro del header Authorization. Aunque es fácil de implementar, Base64 no cifra los datos, por lo que debe usarse junto con HTTPS para asegurar que la información no sea interceptada.

### API Keys
Algunas APIs usan API Keys para autorizacion. Es un token que el cliente provee cuando hace la llamada via queryString. La key se supone que es secreta y que solo el cliente y el servidor la conocen. Solo deberia usarse en conjunto con otro mecanismo de seguridad como HTTPS/SSL.

Las API Keys son identificadores secretos que el cliente incluye en cada solicitud para autenticarse.

### Token Auth / Bearer Authentication
Utiliza tokens de seguridad llamados Bearer (da acceso al portador del token). Se envia un header de Authorization.

La autenticación con tokens utiliza un token de acceso que el cliente debe incluir en cada solicitud mediante el header Authorization.

### OAuth
OAuth es un protocolo de autenticación que permite delegar la autenticación del usuario a un servicio que gestiona las cuentas. En lugar de pedir al usuario que ingrese su contraseña directamente en una aplicación de terceros, la aplicación solicita permiso al servicio para acceder a los recursos del usuario. El servicio autoriza el acceso y otorga un token de acceso que la aplicación puede usar para interactuar con los datos del usuario de forma segura, sin necesidad de compartir las credenciales del usuario con la aplicación.

Permite a los usuarios conceder acceso a sus datos a aplicaciones de terceros sin compartir sus contraseñas

### JWT
El token se genera en el primer paso del proceso de autenticación y se utiliza para autenticar al usuario en futuras solicitudes. Una de las principales ventajas de JWT es que las credenciales de usuario solo se envían una vez; el token es enviado en cada solicitud posterior, eliminando la necesidad de almacenar el estado del usuario en el servidor.

Este tipo de autenticación mejora la eficiencia de las aplicaciones, ya que evita hacer múltiples llamadas a la base de datos para validar al usuario. 

El JWT está compuesto por tres partes: 
- un header (que especifica el algoritmo de firma),
- un payload (que contiene la información del usuario y otras reclamaciones), y
- una firma (que garantiza la integridad del token).

Todo esto se codifica y se firma, lo que asegura que no puede ser alterado sin invalidar el token.

Los JWT pueden ser mensajes solo firmados, solo encriptados o ambos. 
- Si un token es solo firmado pero no encriptado cualquiera puede leer su contenido, pero si no se conoce la clave privada no puede ser modificado. Ya que al validar la firma no coincidiria.

![image](https://github.com/user-attachments/assets/a22b9cfc-ea55-4e86-aaac-d61fddd66476)

El server valida la firma del JWT para saber que lo que le envio al cliente no se modifico. De esta forma se sigue siendo stateless y generalmente se hace mas eficiente la validacion del usuario, sin tener que acceder a un medio persistente a validar si el token es valido y a quien pertenece.

![image](https://github.com/user-attachments/assets/7de66117-fbdd-41f3-ade0-71bd097450bf)

>La firma en un JWT es como un sello digital que garantiza que el contenido del token no fue alterado desde que fue emitido por el servidor. Cuando se genera un JWT, el servidor toma el header y el payload, los codifica, y les aplica un algoritmo de firma (como HMAC o RSA) usando una clave secreta (o una clave privada si se usa firma asimétrica). El resultado es un hash que se adjunta como la tercera parte del token.

> Cuando el cliente luego envía ese token al servidor en una solicitud, el servidor vuelve a calcular esa firma con su clave secreta y compara ambas versiones. Si coinciden, significa que el token no fue modificado por nadie y es confiable. Si no coinciden, se descarta.

### Refresh Tokens
Dado que los access tokens deben tener un tiempo de vida limitado por razones de seguridad, se introduce el concepto de refresh token. Este es otro tipo de token, de un solo uso, que permite al cliente obtener un nuevo access token sin necesidad de volver a enviar las credenciales del usuario. Así se mantiene la sesión activa sin comprometer la seguridad, ya que las credenciales originales solo se utilizan una vez.

## Versionado
Se refiere a la práctica de gestionar y comunicar los cambios a lo largo del tiempo. Es decir, cuando una API evoluciona —por ejemplo, porque se agregan funcionalidades, se cambian estructuras de datos o se eliminan comportamientos anteriores—, es necesario indicar qué versión está usando cada cliente para evitar errores o incompatibilidades.

Rest no provee un mecanismo definido para versionado pero se suelen ver estas estrategias:
- usando la URI
- usando un Custom Header: enviar la versión a través de un header 
- usando el Header Accept: para especificar el formato y la versión deseada de la respuesta

## Hateoas
La idea principal es que cuando un cliente (como una app o un navegador) recibe datos de un servidor, esos datos no solo contienen la información solicitada, sino también los enlaces (links) hacia las siguientes acciones posibles que puede realizar sobre esos datos. De esta forma, el cliente puede descubrir qué puede hacer a continuación simplemente siguiendo los enlaces proporcionados, sin necesidad de "saber" de antemano cómo funciona toda la API.

>Significa que la información sobre cómo interactuar con un recurso se encuentra dentro de la respuesta del recurso mismo, en forma de enlaces hipertextuales

## Respuestas
Las respuestas de una API deben mantenerse lo más estandarizadas posible. Es importante devolver solo los datos necesarios para no sobrecargar al cliente, y usar correctamente los códigos de estado HTTP para reflejar el resultado de la operación (como 200 OK, 404 Not Found, 401 Unauthorized, etc.).

## Paginado, filtros y ordenamientos
Los filtros y el ordenamiento de resultados suelen aplicarse a través de parámetros en la query string o dentro del cuerpo de la solicitud.

Paginado es no devolver toda la base de datos sino x cantidad de registros

## Logging, health y metrics
Tener logs, metricas y puntos de control ayudan a detectar los problemas antes de que realmente lleguen. Se suelen agregar endpoints para vefificar o monitorear que la API este viva, y obtener datos de uso de memoria, etc.

`/health`

`/metrics`

<div style="page-break-after: always;"></div>

# Kata
Es una actividad, es un ejercicio de programación diseñado para ser repetido muchas veces con el objetivo de perfeccionar habilidades.

El objetivo no es llegar a una respuesta correcta, sino lo que se aprende en el camino, el objetivo es la practica no la solucion.

# Coding Dojo
Un lugar seguro para practicar katas de forma colaborativa. Un lugar para hacer errores y aprender. Juntarnos para trabajar en una kata, pasarlo bien y practicar.

# Refactoring
Una técnica para reestructurar un cuerpo de código existente, alterando su estructura interna sin cambiar su comportamiento externo.

Se quieren tests unitarios para garantizar que el comportamiento externo no se modifico y luego aplicar las refactorizaciones propuestas

Para refactorizar:
- Asegurarse de que pasen los tests
- Encontrar code smells:
    - codigo duplicado
    - una funcion muy larga
    - clase con muchos metodos
    - una funcion con muchos parametros
    - clase divergente: ocurre cuando una clase o módulo se modifica con frecuencia por motivos diversos y no relacionados entre sí
    - shotgun surgery: mucho acoplamiento
    - feature envy: cuando una clase utiliza con frecuencia los métodos, propiedades o datos de otra clase
    - data clumps:cuando varios métodos o clases usan los mismos conjuntos de parámetros 
    - obsesion primitiva: cuando se abusa de tipos primitivos (como int, string, float, etc.) en vez de usar objetos que representen conceptos
    - usar switch
    - lazy class: una clase con una sola funcion
    - cadena de mensajes: `pedido.getCliente().getDireccion().getCiudad()`
    - data class: getters y setters pero sin comportamiento

# TDD 
![image](https://github.com/user-attachments/assets/48801ded-c2f5-4523-8d03-fa2077a9e02f)

1. **Write a test that fails**: Escribir una prueba antes de escribir el código real. Esta prueba define lo que espero que el código haga, pero como aún no lo esta implementado, fallará.
2. **Make the code work**: Escribir el código más simple posible para que esa prueba pase.
3. **Eliminate redundancy**: Con la prueba pasando, ahora se puede refactorizar con la seguridad de que si se rompe algo, las pruebas lo mostraran. Al final, el código debe ser más limpio y seguir pasando la prueba.

## Las 3 leyes de TDD
1. No podes escribir codigo productivo a menos que haya un test fallando
2. No podes escribir mas de un test unitario del que es suficiente para fallar
3. No podes escribir mas codigo productivo del que es suficiente para pasar el test que falla


<div style="page-break-after: always;"></div>

# Docker 

Docker es una herramienta que automatiza el despliegue de aplicaciones aisladas dentro de contenedores

Forma tradicional de desplegar una aplicación:
- Acceder directamente al sistema a configurar
- Copiar código/ejecutable a desplegar
- Usar herramientas interactivas para inspeccionar y modificar el sistema
- Asegurar que todas las dependencias estén presentes

Problemas
- Altamente repetitivo
- Gran probabilidad de error
- Interacciones entre aplicaciones
- Es difícil reconstruir la configuración ("Funciona en mi máquina staging")

### Configuracion de maquinas - Infrastructure as Code
En lugar de realizar modificaciones manualmente, se usa un lenguaje de programación, generalmente declarativo, específico para el dominio de configuraciones de máquinas (Ansible, Chef, Puppet, Terraform)

**Declarativo**: Especifica qué objetivo lograr </br>
**Imperativo**: Especifica cómo lograr el objetivo

![image](https://github.com/user-attachments/assets/c1349815-9132-4987-a4ae-0f6bfbf45dfc)


### Mascota vs Ganado
| Infraestructura Mascota                               | Infraestructura Ganado                                  |
|--------------------------------------------------------|----------------------------------------------------------|
| 🐕<br>- Nombres específicos<br>- Únicas<br>- Cuidadas   | 🐄🐄🐄🐄🐄<br>- Número de serie<br>- Prácticamente idénticas<br>- Reemplazable |
| - Mantenimiento delicado<br>- Presentes aunque no sean necesarios | - "Mantenimiento" creando otra instancia<br>- Se crean y destruyen a necesidad |
| - Servicios legacy<br>- Servicios únicos               | - Servicios sin estado interno relevante                 |


### Maquinas virtuales
Se emula un hardware por abajo del SO "invitado" que es gestionado por un hipervisor (monitor de máquina virtual) que a su vez corre en el sistema operativo que esta sobre su propio hardware

![image](https://github.com/user-attachments/assets/84fa917d-5e95-443b-8738-1a1949002395)

Emulación de una máquina real
- Provee aislamiento total
- Única opción para ejecutar programas de otras arquitecturas de hardware
- Al menos dos sistemas operativos ejecutando

Resulta ser algo lento porque es pesado correr x cantidad de sistemas operativos

### Linux Namespaces
Linux namespaces son una funcionalidad del kernel de Linux que permite aislar recursos del sistema entre procesos. Permiten que un proceso vea y utilice solo una parte de los recursos del sistema, como si fuera el único proceso en el sistema.

| Namespace | Aísla...                                      | Ejemplo en contenedores Docker                                |
|-----------|-----------------------------------------------|----------------------------------------------------------------|
| `pid`     | Procesos                                      | Cada contenedor tiene su propio árbol de procesos              |
| `mnt`     | Sistemas de archivos (mount points)           | Un contenedor tiene su propio sistema de archivos              |
| `net`     | Interfaces de red, IPs, puertos               | Cada contenedor puede tener su propia IP                       |
| `uts`     | Nombre del host y nombre de dominio           | Un contenedor puede tener su propio `hostname`                 |
| `ipc`     | Recursos de comunicación entre procesos       | Aísla colas de mensajes, semáforos, memoria compartida         |

## Contenedores
Linux Namespaces para separar grupos de procesos
- Aislamiento configurable entre aplicaciones
- Usan el mismo kernel que el host
- Overhead mínimo

![image](https://github.com/user-attachments/assets/871a3d46-da7e-4314-bb9d-01d0ebdb8742)

La idea es que en vez de estar trabajando con un segundo SO embebido en el primero, se hace que el mismo kernel del SO anfitrión aísle y gestione los recursos para cada contenedor, simulando entornos separados sin necesidad de virtualización completa.

## Docker
Conceptos: 
- Container: Grupo aislado de procesos
- Image: Template usado para crear contenedores (Sistema de archivos + metadata)
- Dockerfile: Archivo con instrucciones para construir una imagen
- Mounts: Acceso a directorios del host
- Volumes: Area donde se persisten datos

Brinda:
- Consistencia: Cualquier imagen se obtiene, inicia y configura de la misma manera
- Replicabilidad: Los contenedores basados en una misma imagen son inicialmente iguales
- Aislamiento: Se puede controlar la interacción entre la aplicación en un contenedor y el mundo exterior (en ambas direcciones)

![image](https://github.com/user-attachments/assets/3397207a-b306-4c89-8981-f7661662f5e6)

El usuario se comunica con el contenedor a traves de la aplicacion CLI de docker que tiene un cliente REST que se comunica con el servidor REST perteneciente al Docker Daemon

![image](https://github.com/user-attachments/assets/9476f4de-1d9d-4ffd-b363-7642481ed0f6)

### Algunos comandos 

`docker run -v host_dir:container_dir ...`

El comando -v en Docker es para montar volúmenes, es decir, compartir directorios entre el host y el contenedor. El contenedor verá el contenido del host como si fuera suyo.

- Le "monta" un directorio del host dentro del contenedor.
- Lo que esté en host_dir será accesible desde container_dir dentro del contenedor.
- Los cambios hechos dentro del contenedor también se reflejarán en el host (si no es de solo lectura `:ro`).


`docker run -p external_port:internal_port ...`

El comando -p de Docker es para exponer puertos del contenedor al host. Docker redirige los paquetes que llegan al external_port hacia el internal_port del contenedor. Tambien se puede especificar ip en la que se reciben los paquetes. 


# Dockerfile
El ecosistema Docker asume que los contenedores son **livianos**, o sea
- Dedicados a un único propósito: Ejecutan un comando; no incluyen dependencias innecesarias.
-  Mantienen el estado mínimo necesario
-  Pueden encender/apagar rápidamente: Útil para escalar horizontalmente

## Imagenes
![image](https://github.com/user-attachments/assets/0dc0fc96-d8dd-430a-a3ad-f934bf086114)

Las imágenes se almacenan como una referencia a la imagen anterior y una lista de diferencias, llamada layer. Cada layer es inmutable.

Para reuso, se asume que cada layer depende solo de:
- Imagen anterior
- El comando ejecutado
- Los archivos usados del directorio del Dockerfile

### Imagenes multi-etapa
Separa la construcción de una imagen en diferentes etapas

Cada etapa: 
- parte de una nueva imagen base
- se puede construir en paralelo con otras etapas

Permite copiar archivos de una etapa a otra y es usado para no incluir compiladores/linters/etc en runtime

## Seguridad
- El control de acceso a archivos es por id de usuario
- El sistema de archivos solo almacena numeros de id de usuario
- Un contenedor puede ejecutar con cualquier id de usuario que quiera

Cualquier usuario con permiso de crear contenedores puede escalar a ser root `docker run -it -v /:/host ubuntu`

## Orquestadores
Un orquestador coordina el uso de múltiples contenedores para implementar una única aplicación, brindando:
- Configuración de contenedores heterogéneos
- Distribución
- Balanceo de carga
- Tolerancia a fallos

Ejemplos: docker compose, kubernetes

<div style="page-break-after: always;"></div>

# Git

Sistema de control de versiones distribuido (Ningún cliente está privilegiado (tecnológicamente) sobre otros). 

Se pueden manejar versiones de un proyecto en secuencia o en paralelo.

Git es un sistema de control de versiones descentralizado pero hay un repositorio central distinguido:
- Servidor propio
- Forja: servicio que hostea git (github, gitlab, bitbucket, etc). Ademas agregan features secundarias propias que no se pueden transferir entre proveedores: issue trackers, CI/CD, metricas, pull requests, etc

## Commits
Es algun estado del sistema que se quiere conservar para el futuro o compartirlo con el resto del equipo. 

Cada commit contiene
- ancestros
- autor/fecha/commit
- mensaje de commit
- archivos

### Mensajes de commit
![image](https://github.com/user-attachments/assets/53a9b00a-366d-4b54-b08c-1326e0b7e491)

No debe pasar:
![image](https://github.com/user-attachments/assets/a777a402-e8b7-474d-971a-d379774ff6fa)

### Commits atomicos
Un commit que aplica un cambio completo.
- Una sola razón para todo lo que cambió
- No depende de cambios posteriores

Facilita manejar commits:
- Revertir
- Reordenar
- Búsquedas en la historia

No hay relación entre tamaño de commit y atomicidad del mismo

### Historia
Cada commit tiene ancestros. Su contenido está relacionado al contenido de sus ancestros. Único requisito: Sin ciclos.

![image](https://github.com/user-attachments/assets/d2a4bfa0-1278-4d1c-b907-d7a9236527c3)

Git no impone una organización de la historia. El equipo debe decidir cómo organizarse

### Trunk-based
Todo cambio se agrega a un mismo branch

![image](https://github.com/user-attachments/assets/8ce801a5-b975-4c3f-9734-8838533fd9b0)

Ventajas:
- Simple
- Todo el código está en el último commit

Desventajas:
- Todo el código está en el último commit
- Cuesta separar de líneas de trabajo

Múltiples desarrolladores pueden trabajar sobre el mismo código simultáneamente, sin posibilidad de fingir que su trabajo fue secuencial

#### Conflicto
Al hacer merge, hay conflicto cuando los cambios de cada rama interactúan de forma negativa.
- Conflicto textual: Mismas líneas ⇒ git puede detectarlo
- Conflicto semántico: Misma lógica ⇒ requiere analizar la interacción

Deseamos que los conflictos sean textuales

### Feature Branches
Un branch por funcionalidad de código independiente

![image](https://github.com/user-attachments/assets/1d4cdf09-dac0-4773-8ef3-ae01aadbb92a)

Ventajas:
- Solo un feature incompleto por branch
- Menos gente trabajando en cada branch
- El resto del equipo ve todos los cambios juntos
Desventajas:
- Administración de branches
- Features necesitan ser independientes entre sí

### Pull Requests (o merge requests)
Antes de hacer un merge, hay oportunidad de verificar:
− Calidad del código
− Calidad de la aplicación
− Cumplimiento de requerimientos
− Si el cambio conviene

Para iniciar estas verificaciones, existe el proceso de Pull Request

Un buen PR: 
- Es atomico: una sola razón para todo lo que cambió; No depende de cambios externos
- Explica: Razones que no resultan obvias del resumen; Efectos de los cambios que no resultan obvios al ver el código

![image](https://github.com/user-attachments/assets/1572210e-da26-46bc-847b-94223c7a609b)

### Branches a largo plazo
Si mantenemos un branch separando durante demasiado tiempo:
- Bugs hallados y arreglados en ambos branches
- Hay que reconciliar los conflictos

No hay que hacer branches a largo plazo. Para evitarlo:
- Modularizar mejor: Separar variantes por archivo en lugar de por branch
- Feature flags: Activar una u otra sección de código por configuración
- Excepción: **Branches de Entorno**: Es una branch que representa un entorno de despliegue: nombres: production, main, master, dev, etc

## Git Flow vs GitHub Flow
- **Git Flow**: Estructura compleja, ideal para grandes proyectos o software con versiones estables y bien definidas. Usa múltiples ramas principales:
  - `master`: versiones estables y en produccion
  - `develop`: codigo que esta en desarollo, lo que se va a convertir en la proxima version estable
  - `feature/`, `release/`, `hotfix/`</br?
  Hay una verificacion al preparar cada release. Es software con despliegues complejos-lentos-caros

![image](https://github.com/user-attachments/assets/10790b4d-17ad-40ee-8e77-53d6abc78840)

- **GitHub Flow**: Estructura simple, pensada para desarrollo ágil y despliegue continuo. Solo una rama principal: `main` (o `master`), siempre contiene el código listo para producción. Cada cambio se hace en una rama nueva que parte de main, y se revisa mediante un pull request antes de integrarse. </br>
   La verificación es dentro de cada PR.

## Monorepo vs Polirepo
- **Monorepo**: Un repositorio para todo el proyecto. Es simple, facilita hacer cambios coordinados a N componentes.
- **Polirepo**: Un repositorio por componente del proyecto. Permite control de acceso limitando autorización a
ciertos repositorios; facilita modularizar componentes

## Integracion continua - CI/CD
**Continuous Integration**: Cada vez que alguien hace un cambio (push), se ejecutan pruebas, se compila el código y se verifica que todo sigue funcionando.
- Integrar frecuentemente el trabajo realizado
- Descubrir errores rápidamente
- De forma automatica

**Continuous Deployment**: Automatizar la entrega del software. Una vez que el código está probado y aprobado, se puede enviar automáticamente a producción o a un entorno de pruebas.
- Asegurar que podemos producir un entregable de forma rápida y certera
- Desplegar a entornos de prueba/producción
- De forma automatica

- Artefacto: Algún archivo que deseamos usar fuera del build. Es cualquier archivo generado en el proceso de CI/CD que se necesita para la siguiente etapa.
- Runners: es el servidor o entorno donde se ejecuta el pipeline de CI/CD. El runner agarra el código, instala dependencias, corre tests, compila, empaqueta, despliega, etc. Puede estar en algún servidor que provee el servicio o en algún servidor que configuramos
- Portabilidad: Indicamos que las mismas tareas se ejecuten en múltiples entornos. Significa que la aplicación pueda correr igual en distintos entornos.

### Uso con docker
Dos formas de usar docker para determinar el entorno en que ejecuta un build:
- Build crea una imagen docker docker push a un registro
- Ejecutar build dentro de un contenedor. Extraer artefactos del contenedor

En ambos casos, docker hace a los builds independientes del runner

<div style="page-break-after: always;"></div>

# Patrones de diseño
**Creational patterns** provide object creation mechanisms that increase flexibility and reuse of existing code.

**Structural patterns** explain how to assemble objects and classes into larger structures, while keeping these structures flexible and efficient.

**Behavioral patterns** take care of effective communication and the assignment of responsibilities between objects.


# Patrones creacionales
Se enfocan en cómo crear objetos, separando el proceso de creación de su uso. Abordan el problema de cómo crear objetos de manera flexible y reutilizable, proporcionando mecanismos para la creación de objetos que no se basan en la creación directa de objetos. 

## Factory
**Aplicabilidad**: 
- Cuando desde una clase se desee crear y usar objetos sin que la misma quede acoplada a las clases de estos.
- Cuando una clase no pueda anticipar la clase de objetos que debe crear.
- Cuando una clase quiera que sean sus subclases las que especifiquen los objetos que crea.

### Estructura

![image](https://github.com/user-attachments/assets/01fbcbc5-c789-4062-9714-e7ea87c8b27a)

- **Product** declara la interfaz, que es comun a todos los objetos que puede producir la clase creadora y sus subclases
- Los **ConcreteProduct** son distintas implementaciones de Product
- La clase **Creator** declara el metodo factory que devuelve nuevos objetos de producto. Coincide el tipo de retorno con el tipo de la interfaz de producto
- Los **ConcreteCreators** sobreescriben el Factory Method, devolviendo un tipo diferente de producto

*Efectos deseados*: El patrón sigue el Principio de Responsabilidad Única (la creación de los
objetos se concentra en las fábricas). Se disminuye el acoplamiento entre las clases. Y sigue el Principio de abierto/cerrado. Puedes incorporar nuevos tipos de productos en el programa sin descomponer el código cliente existente.

### Ejemplo 1
**Situacion**: Una aplicación de mensajería fue diseñada inicialmente solo para enviar correos electrónicos. Toda la lógica de envío de mensajes, validación y formato estaba escrita directamente en una clase MensajeEmail.

Los usuarios comenzaron a solicitar otros tipos de mensajes, como SMS y WhatsApp. Para agregarlos, el equipo tuvo que llenar el código de condicionales que preguntaban por el tipo de mensaje: `"si es email, hacer esto... si es SMS, hacer esto otro..."`. Esto hizo que el sistema fuera difícil de mantener, difícil de escalar, y muy propenso a errores cada vez que se quería agregar un nuevo tipo de mensaje.

El problema central era que el código estaba fuertemente **acoplado** a los tipos concretos de mensajes. Cada vez que se agregaba uno nuevo, era necesario modificar varias partes del sistema, violando el principio de abierto/cerrado (el código debería estar abierto a la extensión pero cerrado a la modificación).

**Solución**: En vez de instanciar directamente (new MensajeEmail()), delegamos la creación del objeto a un método fábrica. Este método es declarado en una clase abstracta (o interfaz), y cada tipo de mensaje tendrá su propia clase que implemente ese método, devolviendo el objeto adecuado.

**En codigo**

- **Product**
```
public interface Mensaje {
    void enviar(String destinatario, String contenido);
}
```
- **ConcreteProduct**
```
public class MensajeEmail implements Mensaje {
    public void enviar(String destinatario, String contenido) {
        System.out.println("Enviando Email a " + destinatario + ": " + contenido);
    }
}

public class MensajeSMS implements Mensaje {
    public void enviar(String destinatario, String contenido) {
        System.out.println("Enviando SMS a " + destinatario + ": " + contenido);
    }
}
```
- **Creator**
```
public abstract class MensajeFactory {
    // Método Factory
    public abstract Mensaje crearMensaje();
}
```
- **ConcreteCreator**
```
public class EmailFactory extends MensajeFactory {
    public Mensaje crearMensaje() {
        return new MensajeEmail();
    }
}

public class SMSFactory extends MensajeFactory {
    public Mensaje crearMensaje() {
        return new MensajeSMS();
    }
}
```
- **Cliente**
```
public class Main {
    public static void main(String[] args) {
        MensajeFactory factory = new EmailFactory();  // puede cambiarse por SMSFactory
        Mensaje mensaje = factory.crearMensaje();
        mensaje.enviar("ana@example.com", "Hola Ana!");
    }
}
```


## Abstract Factory
**Aplicabilidad**
- Cuando un sistema deba ser independiente de cómo se crean, componen y representan sus productos.
- Cuando un sistema deba ser configurado con una familia de productos de entre varias.
- Cuando una familia de objetos producto relacionados esté diseñada para ser usada conjuntamente, y sea necesario hacer cumplir esta restricción.
- Cuando se quiera proporcionar una biblioteca de clases de productos, y solo se quiera revelar sus interfaces, no sus implementaciones

### Estructura

![image](https://github.com/user-attachments/assets/4e57c3d4-0f34-45d9-84e6-01ea069573e8)

- Los **AbstractProduct** declaran interfaces para un grupo de productos diferentes pero relacionados que forman una familia de productos
- Los **Products**, productos concretos, son las distintas implementaciones de productos abstractos agrupados por variantes. Cada producto abstracto debe implementarse en todas las variantes dadas
- La **AbstractFactory** declara un grupo de metodos para crear cada uno de los productos abstractos
- Las **ConcreteFactory** implementan los métodos de creación de la fábrica abstracta. Cada fábrica concreta se corresponde con una variante específica de los productos y crea tan solo dichas variantes de los productos.
 -El **Cliente** puede funcionar con cualquier variante fábrica/producto concreta, siempre y cuando se comunique con sus objetos a través de interfaces abstractas.
  
### Ejemplo 1
**Situacion**: Una empresa está desarrollando una aplicación de interfaz gráfica que debe poder funcionar en Windows y en Mac. Al principio, todo fue hecho para Windows, y se usaban botones, menús y ventanas específicas de Windows.

Cuando se quiso soportar Mac, el equipo se dio cuenta de que el código estaba lleno de condicionales como if (sistema == WINDOWS) y if (sistema == MAC), para decidir qué componente gráfico usar.
Esto hizo el código difícil de mantener, muy repetitivo, y frágil ante cambios.

El problema era que todo el sistema estaba acoplado a familias de objetos concretos: botones, menús, ventanas específicas de cada sistema operativo.

**Solucion**: Definir una familia de objetos relacionados (por ejemplo, todos los componentes gráficos de Windows o de Mac) mediante una interfaz común, y delegar la creación de todos ellos a una fábrica abstracta. Así se pueden crear objetos sin que el cliente tenga que saber qué sistema operativo se está usando.

**En codigo**: interfaz gráfica con dos temas: TemaClaro y TemaOscuro. Cada tema tiene su Botón y su Menú.
- **AbstractProduct**
```
public interface Boton {
    void dibujar();
}

public interface Menu {
    void desplegar();
}
```
- **Product**
```
public class BotonClaro implements Boton {
    public void dibujar() {
        System.out.println("Dibujando botón claro");
    }
}

public class BotonOscuro implements Boton {
    public void dibujar() {
        System.out.println("Dibujando botón oscuro");
    }
}

public class MenuClaro implements Menu {
    public void desplegar() {
        System.out.println("Mostrando menú claro");
    }
}

public class MenuOscuro implements Menu {
    public void desplegar() {
        System.out.println("Mostrando menú oscuro");
    }
}
```
- **AbstractFactory**
```
public interface GUIFactory {
    Boton crearBoton();
    Menu crearMenu();
}
```
- **ConcreteFactory**
```
public class TemaClaroFactory implements GUIFactory {
    public Boton crearBoton() {
        return new BotonClaro();
    }

    public Menu crearMenu() {
        return new MenuClaro();
    }
}

public class TemaOscuroFactory implements GUIFactory {
    public Boton crearBoton() {
        return new BotonOscuro();
    }

    public Menu crearMenu() {
        return new MenuOscuro();
    }
}
```
- **Client**
```
public class Aplicacion {
    private Boton boton;
    private Menu menu;

    public Aplicacion(GUIFactory factory) {
        boton = factory.crearBoton();
        menu = factory.crearMenu();
    }

    public void mostrarUI() {
        boton.dibujar();
        menu.desplegar();
    }

    public static void main(String[] args) {
        GUIFactory factory = new TemaOscuroFactory(); // cambia por TemaClaroFactory
        Aplicacion app = new Aplicacion(factory);
        app.mostrarUI();
    }
}
```
- **Main**
```
public class Main {
    public static void main(String[] args) {
        GUIFactory factory;

        // Supongamos que detectamos tema oscuro
        factory = new TemaOscuroFactory();  // 👈🏼 decide la variante

        Aplicacion app = new Aplicacion(factory);  // 👈🏼 se inyecta la fábrica
        app.dibujarUI();  // 👈🏼 la app usa los productos, sin saber cuáles
    }
}
```

## Builder
Nos permite construir objetos complejos paso a paso. El patrón nos permite producir distintos tipos y representaciones de un objeto empleando el mismo código de construcción.

**Aplicabilidad**
- Para evitar un “constructor telescópico”. Digamos que tenemos un constructor con diez parámetros opcionales. Invocar a semejante bestia es poco práctico, por lo que sobrecargamos el constructor y creamos varias versiones más cortas con menos parámetros
```
class Pizza {
    Pizza(int size) { ... }
    Pizza(int size, boolean cheese) { ... }
    Pizza(int size, boolean cheese, boolean pepperoni) { ... }
    // ...
```
- Cuando el objeto se puede construir de varias formas.
- Cuando es complicado de instanciar con un solo constructor largo.
- Cuando tiene muchos atributos opcionales o configurables.


### Estructura

![image](https://github.com/user-attachments/assets/e8eb49c0-fdae-429d-9c86-88042c2d6898)

- La interfaz **Builder** declara pasos de la construccion de un producto que todos los tipos de objetos builder tienen en comun
- Los **ConcreteBuilder** son distintas implementaciones de los pasos de construccion
- Los **Product** son los objetos resultantes. Los productos construidos por distintos objetos constructores no tienen que pertenecer a la misma jerarquía de clases o interfaz.
- La clase directora **Director** define el orden en el que se invocaran los pasos de construccion. Es opcional
- El **Client** debe asociar uno de los objetos constructores con la clase directora

### Ejemplo 1
**Situación**: Querés crear reportes PDF en una app. Algunos tienen portada, otros no. Algunos tienen pie de página, otros gráficos, otros resumen, etc. Si tratás de hacerlo todo con un constructor, queda algo horrible como: `new Reporte(true, false, true, null, "Título", null, true, false, ...)`. </br>
Y además, si querés cambiar la forma de construir un reporte, tenés que modificar el código del `Reporte` mismo.

**Problema**: El constructor es inmanejable y no es claro qué representa cada parámetro. Es difícil extender y mantener. Además, no podés crear distintas “versiones” del reporte sin meter muchos if.

**Solución**: Separar el objeto que se construye (por ejemplo, Reporte) del proceso de construcción. Así, podés tener distintos "constructores paso a paso" (Builders) que arman reportes distintos de manera más clara. El patrón Builder sugiere que saques el código de construcción del objeto de su propia clase y lo coloques dentro de objetos independientes llamados constructores.

### Ejemplo 2
**Situacion**: Estás desarrollando una aplicación de diseño de casas. Cada casa puede tener distintas configuraciones: algunas tienen paredes de ladrillo, otras de mármol, unas tienen piscina, otras no, unas tienen techo de tejas, otras de vidrio, etc. A medida que el sistema creció, cada casa empezó a tener más opciones: jardín, garage, piso, ventanas, paneles solares, alarma, etc. El constructor empezó a tener más y más parámetros. El código quedó difícil de entender y mantener: `Casa casa = new Casa("mármol", "vidrio", true, true, false, "roble", true, false, false, true);`. Y si querías construir diferentes tipos de casa (moderna, simple, lujosa), tenías que meter if y switch por todos lados o duplicar código.

**Solucion**: El patrón Builder permite construir paso a paso objetos complejos como Casa, separando la lógica de construcción de la estructura del objeto.

Así podés tener distintos "constructores" (CasaDeLujoBuilder, CasaEstandarBuilder) que implementan la misma interfaz y que saben cómo construir cada tipo de casa.

Luego, un Director (como Ingeniero) usa ese builder para ensamblar la casa siguiendo un orden definido

**En codigo**
- **Product**
```
class Casa {
    String paredes;
    String techo;
    boolean piscina;

    public void mostrar() {
        System.out.println("Casa con: " + paredes + ", " + techo + ", piscina: " + piscina);
    }
}
```
- **Builder**
```
interface CasaBuilder {
    void construirParedes();
    void construirTecho();
    void construirPiscina();
    Casa obtenerResultado();
}
```
- **ConcreteBuilder**: para una casa de tipo "De Lujo"
```
class CasaDeLujoBuilder implements CasaBuilder {
    private Casa casa = new Casa();

    public void construirParedes() {
        casa.paredes = "Paredes de mármol";
    }

    public void construirTecho() {
        casa.techo = "Techo de vidrio";
    }

    public void construirPiscina() {
        casa.piscina = true;
    }

    public Casa obtenerResultado() {
        return casa;
    }
}
```
- **Director**
```
class Ingeniero {
    private CasaBuilder builder;

    public Ingeniero(CasaBuilder builder) {
        this.builder = builder;
    }

    public Casa construirCasa() {
        builder.construirParedes();
        builder.construirTecho();
        builder.construirPiscina();
        return builder.obtenerResultado();
    }
}
```
- **Client**
```
public class Main {
    public static void main(String[] args) {
        CasaBuilder builder = new CasaDeLujoBuilder();
        Ingeniero director = new Ingeniero(builder);

        Casa casa = director.construirCasa();
        casa.mostrar();
    }
}
```

### Builder vs Factory
![image](https://github.com/user-attachments/assets/ba6cec00-0e9d-4b06-9fff-3f3fa8ba3b3b)

## Singleton
El patrón Singleton asegura que una clase tenga una única instancia en todo el sistema, y proporciona un punto de acceso global a esa instancia.

**Aplicabilidad**
- Cuando se necesita que solo exista una unica instancia de algo
- CUando se necesita compartir un recurso global

El patrón Singleton resuelve dos problemas al mismo tiempo, vulnerando el *Principio de responsabilidad única*:
1. Garantizar que una clase tenga una única instancia. ¿Por qué querría alguien controlar cuántas instancias tiene una clase? El motivo más habitual es controlar el acceso a algún recurso compartido, por ejemplo, una base de datos o un archivo.
2. Proporcionar un punto de acceso global a dicha instancia. Al igual que una variable global, el patrón Singleton nos permite acceder a un objeto desde cualquier parte del programa. No obstante, también evita que otro código sobreescriba esa instancia.


### Estructura

![image](https://github.com/user-attachments/assets/341462fd-a267-4b4f-8130-86d1b4f749f3)

La clase **Singleton** declara el método estático obtenerInstancia que devuelve la misma instancia de su propia clase.

El constructor del Singleton debe ocultarse del código cliente. La llamada al método obtenerInstancia debe ser la única manera de obtener el objeto de Singleton.

### Ejemplo 1
```
public class Configuracion {

    // 1. Instancia única, privada y estática
    private static Configuracion instancia;

    // 2. Constructor privado
    private Configuracion() {
        System.out.println("Cargando configuración...");
    }

    // 3. Método público de acceso (lazy + sincronizado)
    public static synchronized Configuracion getInstance() {
        if (instancia == null) {
            instancia = new Configuracion();
        }
        return instancia;
    }

    // Método de ejemplo
    public void mostrar() {
        System.out.println("Configuración en uso");
    }
}
```
Uso:
```
public class Main {
    public static void main(String[] args) {
        Configuracion c1 = Configuracion.getInstance();
        Configuracion c2 = Configuracion.getInstance();

        c1.mostrar();

        System.out.println(c1 == c2);  // true, es la misma instancia
    }
}
```

# Patrones estructurales
Son soluciones reutilizables que ayudan a resolver problemas comunes en la construcción de software al definir cómo se componen las clases y objetos para crear estructuras complejas. Se enfocan en la estructura de clases y objetos, utilizando herramientas para ensamblar objetos y clases en estructuras más grandes. 

Facilitan el diseño al identificar una forma simple de realizar relaciones entre entidades

## Composite
Permite componer objetos en estructuras de árbol y trabajar con esas estructuras como si fueran objetos individuales.

**Aplicabilidad**:
- Utiliza el patrón cuando quieras que el código cliente trate elementos simples y complejos de la misma forma.
- El uso del patrón Composite sólo tiene sentido cuando el modelo central de tu aplicación puede representarse en forma de árbol.

### Estructura
![image](https://github.com/user-attachments/assets/5af9fd47-4645-4667-af50-07e5d4f24f8f)

- La interfaz **Component** describe operaciones que son comunes a elementos simples y complejos del árbol.
- La **Leaf** es un elemento basico del arbol, que no tiene subelementos
- El **Composite** es un elemento que tiene subelementos: hojas u otros compuestos. Un compuesto no conoce las clases concretas de sus hijos. Funciona con todos los subelementos únicamente a través de la interfaz **Component**.
- El **Client** funciona con todos los elementos a través de la interfaz componente. Como resultado, el cliente puede funcionar de la misma manera tanto con elementos simples como complejos del árbol.

### Ejemplo 1
**Situacion**: Querés representar una estructura jerárquica como un árbol de archivos y carpetas. Cada carpeta puede contener tanto archivos como otras carpetas. El cliente necesita ejecutar operaciones como "mostrar nombre" o "calcular tamaño" sin preocuparse de si está tratando con un archivo o con una carpeta.

**Problema**: El cliente debe realizar operaciones sobre elementos simples (archivos) y compuestos (carpetas), pero el código se llena de condicionales como if (esArchivo) o if (esCarpeta) para distinguir el tipo de elemento y aplicar la operación correspondiente.

**Solucion**: El patrón Composite propone usar una interfaz común (Component) para que tanto hojas como compuestos implementen los mismos métodos. Así, el cliente puede tratarlos de forma uniforme, sin saber si está operando sobre una hoja o un compuesto.

**En codigo**:
**Component**
```
interface Componente {
    void mostrar();
}
```
**Leaf**
```
class Archivo implements Componente {
    private String nombre;

    public Archivo(String nombre) {
        this.nombre = nombre;
    }

    public void mostrar() {
        System.out.println("Archivo: " + nombre);
    }
}
```
**Component**
```
class Carpeta implements Componente {
    private String nombre;
    private List<Componente> hijos = new ArrayList<>();

    public Carpeta(String nombre) {
        this.nombre = nombre;
    }

    public void agregar(Componente componente) {
        hijos.add(componente);
    }

    public void mostrar() {
        System.out.println("Carpeta: " + nombre);
        for (Componente c : hijos) {
            c.mostrar();
        }
    }
}
```
**Client**
```
public class Main {
    public static void main(String[] args) {
        Componente archivo1 = new Archivo("foto.jpg");
        Componente archivo2 = new Archivo("cv.pdf");

        Carpeta carpetaPersonal = new Carpeta("Personal");
        carpetaPersonal.agregar(archivo1);
        carpetaPersonal.agregar(archivo2);

        Componente archivo3 = new Archivo("codigo.java");
        Carpeta carpetaTrabajo = new Carpeta("Trabajo");
        carpetaTrabajo.agregar(archivo3);
        carpetaTrabajo.agregar(carpetaPersonal);

        carpetaTrabajo.mostrar();
    }
}
```

## Decorator
Añade dinámicamente nuevas responsabilidades a un objeto, proporcionando una alternativa
flexible a la herencia para extender la funcionalidad.

**Aplicabilidad**: 
- Cuando se desee añadir responsabilidades a objetos individuales de forma dinámica y transparente, es decir, sin afectar a otros objetos.
- Cuando se desee que las responsabilidades puedan ser retiradas.
- Cuando la extensión mediante la herencia no es viable (a veces es posible tener un gran número de extensiones independientes, produciéndose una explosión de subclases para permitir todas las combinaciones).

“Wrapper” es el sobrenombre alternativo del patrón Decorator. Un *wrapper* es un objeto que puede vincularse con un objeto *objetivo*. El wrapper contiene el mismo grupo de métodos que el objetivo y le delega todas las solicitudes que recibe. No obstante, el wrapper puede alterar el resultado haciendo algo antes o después de pasar la solicitud al objetivo.

El patrón Decorator envuelve (o “decora”) un objeto original en otro objeto que añade o modifica la funcionalidad del primero.

### Estructura

![image](https://github.com/user-attachments/assets/1e7fddca-ea96-4239-ab98-24df34514969)

- **Component** declara la interfaz comun tanto para wrappers como para objetos envueltos
- El **ConcreteComponent** es una clase de objetos que seran envueltos. Define el comportamiento basico que sera alterado por los decorators
- La clase **BaseDecorator** tiene un campo que referencia un objeto envuelto. Su función es delegar las llamadas al objeto encapsulado
- Los **ConcreteDecorator** definen comportamiento extra que se le puede agregar al componente dinamicamente. Hacen un override de los metodos del base decorator. Extienden la clase BaseDecorator y añaden responsabilidades extra antes o después de delegar la llamada al componente.
- El **Client** puede wrappear componentes en multiples capas de decorators

*Efectos deseados*: El patrón ofrece más flexibilidad que la herencia estática (ofrece un enfoque para añadir responsabilidades que consiste en pagar solo por aquello que se necesita). El patrón permite seguir el Principio de Responsabilidad Única.


### Analogia 1
Vestir ropa es un ejemplo del uso de decoradores. Cuando tienes frío, te cubres con un suéter. Si sigues teniendo frío a pesar del suéter, puedes ponerte una chaqueta encima. Si está lloviendo, puedes ponerte un impermeable. Todas estas prendas “extienden” tu comportamiento básico pero no son parte de ti, y puedes quitarte fácilmente cualquier prenda cuando lo desees.

[https://refactoring.guru/es/design-patterns/decorator#:~:text=Vestir%20ropa%20es,cuando%20lo%20desees.]


### Ejemplo 1
**Situacion**: Una aplicación de mensajería permite enviar mensajes de texto. Inicialmente, los mensajes son simples. Con el tiempo, se quiere permitir que los mensajes se puedan: Enviar en negrita (<b>Hola</b>); Encriptar su contenido para mayor seguridad; Añadir otras decoraciones como emoji, marcas de tiempo, etc. Pero no todos los mensajes deben tener todas las funcionalidades. A veces se quiere enviar uno solo con negrita, a veces solo encriptado, a veces con ambas cosas, etc.

**Problema**: Si intentás resolver esto con herencia, tendrías que crear muchas combinaciones: MensajeSimple, MensajeNegrita, MensajeEncriptado, MensajeNegritaYEncriptado, MensajeEmojiYEncriptadoYTimestamp

**Solucion**: El patrón Decorator permite añadir funcionalidad a los objetos de forma flexible y dinámica, sin crear nuevas subclases para cada combinación. En lugar de usar herencia para cada caso, envolvés el mensaje simple en decoradores que agregan comportamiento.

**En codigo**
- **Component**
```
public interface Mensaje {
    String enviar();
}
```
- **ConcreteComponent**
```
public class MensajeSimple implements Mensaje {
    private String contenido;

    public MensajeSimple(String contenido) {
        this.contenido = contenido;
    }

    @Override
    public String enviar() {
        return contenido;
    }
}
```
- **BaseDecorator**
```
public abstract class MensajeDecorator implements Mensaje {
    protected Mensaje mensajeDecorado;

    public MensajeDecorator(Mensaje mensajeDecorado) {
        this.mensajeDecorado = mensajeDecorado;
    }

    @Override
    public String enviar() {
        return mensajeDecorado.enviar();
    }
}
```
- **ConcreteDecorator**: decorador para negrita y otro para encriptar 
```
public class MensajeNegritaDecorator extends MensajeDecorator {

    public MensajeNegritaDecorator(Mensaje mensajeDecorado) {
        super(mensajeDecorado);
    }

    @Override
    public String enviar() {
        // Aplica formato en negrita antes de enviar
        return "<b>" + super.enviar() + "</b>";
    }
}

public class MensajeEncriptadoDecorator extends MensajeDecorator {

    public MensajeEncriptadoDecorator(Mensaje mensajeDecorado) {
        super(mensajeDecorado);
    }

    private String encriptar(String texto) {
        // Algoritmo de encriptación simple (para ejemplo)
        return new StringBuilder(texto).reverse().toString();
    }

    @Override
    public String enviar() {
        // Primero obtiene el contenido del mensaje, luego lo encripta
        return encriptar(super.enviar());
    }
}
```
- **Client**
```
public class Main {
    public static void main(String[] args) {
        // Creamos un mensaje simple
        Mensaje mensaje = new MensajeSimple("Hola, mundo!");

        // Decoramos el mensaje para darle formato en negrita
        mensaje = new MensajeNegritaDecorator(mensaje);

        // Adicionalmente, lo decoramos para encriptarlo
        mensaje = new MensajeEncriptadoDecorator(mensaje);

        // Al enviar el mensaje, se aplica primero la encriptación y luego la negrita según el orden de los decoradores
        System.out.println(mensaje.enviar());
    }
}
```

## Adapter 
Permite la colaboración entre objetos con interfaces incompatibles. Un *adaptador* se trata de un objeto especial que convierte la interfaz de un objeto, de forma que otro objeto pueda comprenderla.

Convierte la interfaz de una clase en otra distinta que es la que esperan los clientes. Permite que cooperen clases que de otra manera no podrían por tener interfaces incompatibles.

**Como funciona**:
1. El adaptador obtiene una interfaz compatible con uno de los objetos existentes.
2. Utilizando esta interfaz, el objeto existente puede invocar con seguridad los métodos del adaptador.
3. Al recibir una llamada, el adaptador pasa la solicitud al segundo objeto, pero en un formato y orden que ese segundo objeto espera.

### Estructura

![image](https://github.com/user-attachments/assets/5ae8a561-4217-4aad-8fb3-93fff677c410)

- El **Client** contiene la lógica de negocio existente del programa.
- La **ClientInterface** describe el protocolo que deben seguir otras clases para poder colaborar con el codigo client.
- El **Service** es una clase 3rd-party o legacy que el cliente no puede usar directamente porque tiene una interfaz incompatible
- El **Adapter** es una clase que puede trabajar tanto con el cliente como con el service: implementa la interfaz del client, y wrappea el service. El adaptador recibe llamadas del cliente a traves de la interfaz del cliente y las traduce en llamadas al service wrappeado en un formato que pueda entender
- El código cliente no se acopla a la clase adaptadora concreta siempre y cuando funcione con la clase adaptadora a través de la interfaz con el cliente. 

### Ejemplo 1
**Situacion**: Una empresa desarrolló una aplicación para gestionar pagos. Esta aplicación usa una interfaz propia (ClientInterface) que define cómo deben realizarse los pagos: pagar(double monto). Todo el código cliente (por ejemplo, la interfaz gráfica, o los controladores) ya trabaja con esta interfaz.

Ahora, quieren integrar un nuevo proveedor de pagos externo (como una API bancaria), que viene con su propia clase NuevoSistemaPago, la cual tiene un método completamente distinto: realizarTransaccion(double cantidad)

**Problema**: El nuevo sistema de pagos no es compatible con la interfaz existente.
No se puede modificar ni el nuevo sistema (porque es una librería externa) ni todo el código cliente (porque sería muy costoso y riesgoso).

**Solucion**: Se aplica el patrón Adapter.
Se crea una clase AdaptadorNuevoSistemaPago que:
- Implementa la interfaz esperada por el cliente (ProcesadorPago).
- Contiene una instancia del nuevo servicio (NuevoSistemaPago).
- Traduce las llamadas de pagar(monto) en llamadas a realizarTransaccion(cantidad).

**En codigo**
- **ClientInterface** — Interfaz que espera el cliente
```
public interface ProcesadorPago {
    void pagar(double monto);
}
```
- **Service**: Clase externa (no modificable) con una interfaz incompatible
```
public class NuevoSistemaPago {
    public void realizarTransaccion(double cantidad) {
        System.out.println("Pago procesado por el NUEVO sistema: $" + cantidad);
    }
}
```
- **Adapter**: Adapta la clase externa al cliente
```
public class AdaptadorNuevoSistemaPago implements ProcesadorPago {
    private NuevoSistemaPago nuevoSistema;

    public AdaptadorNuevoSistemaPago(NuevoSistemaPago nuevoSistema) {
        this.nuevoSistema = nuevoSistema;
    }

    @Override
    public void pagar(double monto) {
        // Adaptamos el método esperado por el cliente al del servicio real
        nuevoSistema.realizarTransaccion(monto);
    }
}
```
- **Client**
```
public class Cliente {
    private ProcesadorPago procesador;

    public Cliente(ProcesadorPago procesador) {
        this.procesador = procesador;
    }

    public void realizarPago(double monto) {
        procesador.pagar(monto);
    }
}
```
- Main
```
public class Main {
    public static void main(String[] args) {
        NuevoSistemaPago sistemaExterno = new NuevoSistemaPago();
        ProcesadorPago adaptador = new AdaptadorNuevoSistemaPago(sistemaExterno);

        Cliente cliente = new Cliente(adaptador);
        cliente.realizarPago(150.0);
    }
}
```


## Proxy
Proporciona un sustituto o representante de otro objeto para controlar el acceso a éste.


### Estructura

![image](https://github.com/user-attachments/assets/aa3f2dfb-bd70-4589-bfe7-ad8ec72b661a)

- La **ServiceInterface** declara la interfaz del **Service**. El **Proxy** debe seguir esta interfaz para poder camuflarse como servicio.
- El **Service** es una clase que provee logica de negocio
- La clase **Proxy** tiene un campo que referencia a un objeto de servicio. Cuando el proxy finaliza su procesamiento, le pasa la request al objeto de servicio
- El **Client** debe funcionar con servicios y proxies a través de la misma interfaz. De este modo puedes pasar un proxy a cualquier código que espere un objeto de servicio.

### Ejemplo 1
**Situacion**: Una empresa tiene un sistema que permite a los usuarios ver documentos confidenciales. Estos documentos están representados por una clase DocumentoReal, que tiene un método ver() para acceder al contenido.

El acceso a los documentos es costoso o sensible (por ejemplo, requieren tiempo de carga, validación, o control de acceso), y no se quiere que cualquier parte del código pueda acceder directamente a ellos.

**Problema**: No se puede controlar quién accede a DocumentoReal; Cargar el contenido del documento cada vez es lento o innecesario si el usuario no tiene permisos; No se quiere modificar DocumentoReal porque ya está en uso y es complejo

**Solucion**: Creamos una clase DocumentoProxy que implementa la misma interfaz que DocumentoReal (Documento); contiene una referencia al DocumentoReal; Controla el acceso al documento real. Asi, el cliente trabaja con la interfaz Documento y no sabe si está usando el documento real o un proxy.

**En codigo**
- **ServiceInterface**: interfaz común entre servicio y proxy
```
public interface Documento {
    void ver();
}
```
- **Service**: clase con la lógica real (costosa o sensible)
```
public class DocumentoReal implements Documento {
    private String nombre;

    public DocumentoReal(String nombre) {
        this.nombre = nombre;
        cargarDesdeDisco();
    }

    private void cargarDesdeDisco() {
        System.out.println("Cargando documento " + nombre + " desde disco...");
    }

    @Override
    public void ver() {
        System.out.println("Mostrando documento: " + nombre);
    }
}
```
- **Proxy**: controla acceso y delega al servicio
```
public class DocumentoProxy implements Documento {
    private DocumentoReal documentoReal;
    private String nombre;
    private boolean tienePermiso;

    public DocumentoProxy(String nombre, boolean tienePermiso) {
        this.nombre = nombre;
        this.tienePermiso = tienePermiso;
    }

    @Override
    public void ver() {
        if (!tienePermiso) {
            System.out.println("Acceso denegado a: " + nombre);
            return;
        }

        if (documentoReal == null) {
            documentoReal = new DocumentoReal(nombre);
        }

        documentoReal.ver();
    }
}
```
- **Client**: trabaja con objetos de tipo ServiceInterface
```
public class Cliente {
    public static void main(String[] args) {
        Documento doc1 = new DocumentoProxy("contrato.pdf", true);
        Documento doc2 = new DocumentoProxy("secreto.pdf", false);

        doc1.ver(); // se permite, carga y muestra
        doc2.ver(); // acceso denegado
    }
}
```

# Patrones de comportamiento
Son patrones que definen cómo los objetos interactúan y se comunican entre sí, centrándose en la asignación de responsabilidades y la implementación de algoritmos. Se enfoca en como las clases y objetos se comunican entre ellas.

## Command
Convierte una solicitud en un objeto independiente que contiene toda la información sobre la solicitud. Esta transformación te permite parametrizar los métodos con diferentes solicitudes, retrasar o poner en cola la ejecución de una solicitud y soportar operaciones que no se pueden realizar

**Aplicabilidad**:
 
### Estructura
![image](https://github.com/user-attachments/assets/e5851b64-c312-4b29-90ff-233da491b7dd)

- La clase **Invoker** (*sender*) es responsable de inicializar las solicitudes.  Esta clase debe tener un campo para almacenar una referencia a un objeto **Command**
- La interfaz **Command** normalmente declara un único método para ejecutar el comando.
- Los **ConcreteCommand** implementan varios tipos de solicitudes. Un comando concreto no se supone que tenga que realizar el trabajo por su cuenta, sino pasar la llamada a uno de los objetos de la lógica de negocio. Sin embargo, para lograr simplificar el código, estas clases se pueden fusionar.
- La clase **Receiver** contiene cierta lógica de negocio. Casi cualquier objeto puede actuar como receptor. La mayoría de los comandos solo gestiona los detalles sobre cómo se pasa una solicitud al receptor, mientras que el propio receptor hace el trabajo real.
-  El **Client** crea y configura los objetos de comando concretos. El cliente debe pasar todos los parámetros de la solicitud, incluyendo una instancia del receptor, dentro del constructor del comando. Después de eso, el comando resultante puede asociarse con uno o varios emisores.

### Ejemplo 1
**Situacion**: Querés construir una interfaz de usuario con botones y menús que realicen acciones como abrir archivos, copiar o pegar texto. Sin embargo, no querés que los botones estén acoplados directamente a funciones específicas como abrirArchivo() o copiar().

**Problema**: Si los botones están directamente conectados a funciones concretas, no podés reutilizar el mismo botón para ejecutar otra acción. Tampoco podrías poner en cola comandos, deshacer operaciones ni cambiar comportamientos dinámicamente.

**Solucion**:Encapsular cada acción dentro de un objeto Command. Estos comandos se pueden pasar a botones (u otros emisores) sin que estos sepan lo que hacen. El botón simplemente ejecuta el comando asociado.

**En codigo**
- **Command**
```
interface Command {
    void ejecutar();
}
```
- **Receiver**
```
class Luz {
    void encender() {
        System.out.println("Luz encendida");
    }
    void apagar() {
        System.out.println("Luz apagada");
    }
}
```
- **ConcreteCommand**
```
class EncenderLuzCommand implements Command {
    private Luz luz;

    public EncenderLuzCommand(Luz luz) {
        this.luz = luz;
    }

    public void ejecutar() {
        luz.encender(); // delega la acción al receptor
    }
}
```
- **Invoker**
```
class ControlRemoto {
    private Command boton1;
    private Command boton2;

    public void setBoton1(Command comando) { this.boton1 = comando; }
    public void setBoton2(Command comando) { this.boton2 = comando; }

    public void presionarBoton1() { boton1.ejecutar(); }
    public void presionarBoton2() { boton2.ejecutar(); }
}

````
- **Client**
```
public class Main {
    public static void main(String[] args) {
        Luz luz = new Luz(); // receptor
        Command encender = new EncenderLuzCommand(luz); // comando

        ControlRemoto control = new ControlRemoto(); // invoker
        control.setBoton1(encender);

        control.presionarBoton1(); // -> "Luz encendida"
    }
}
```




## Strategy
Permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables.

El patrón Strategy sugiere que tomes esa clase que hace algo específico de muchas formas diferentes y extraigas todos esos algoritmos para colocarlos en clases separadas llamadas estrategias.

**Aplicabilidad**:
- Cuando muchas clases relacionadas difieran solo en su comportamiento (las estrategias permiten configurar una clase con un determinado comportamiento de entre muchos posibles).
- Cuando una clase define muchos comportamientos, y estos se representan como múltiples sentencias condicionales en sus operaciones (en vez de tener muchos condicionales, se pueden mover las ramas de estos a su propia clase de estrategia)

### Estructura

![image](https://github.com/user-attachments/assets/72e0d45c-8069-4353-90c2-7e46ceee436d)

- La clase **Context** mantiene una referencia a una de las **ConcreteStrategies** y se comunica con este objeto a traves de la interfaz **Strategy**
- La interfaz **Stretegy** es comun a todas las **ConcreteStrategy**. Declara un método que la clase contexto utiliza para ejecutar una estrategia.
- Las **ConcreteStrategy** implementan variaciones de un algoritmo que utiliza la clase **Context**
- La clase contexto invoca el método de ejecución en el objeto de estrategia vinculado cada vez que necesita ejecutar el algoritmo. La clase contexto no sabe con qué tipo de estrategia funciona
- El **Client** crea un objeto de estrategia específico y lo pasa a la clase contexto. La clase contexto expone un modificador set que permite a los clientes sustituir la estrategia asociada al contexto durante el tiempo de ejecución.

*Efectos deseados*: El patrón sigue el Principio de Responsabilidad Única (organiza en clases
separadas el código relacionado con algoritmos particulares) y el Principio Abierto/Cerrado (es
posible introducir nuevos comportamientos sin cambiar las clases de estrategia existentes o la
clase contexto). Permite aislar los detalles de implementación de un algoritmo del código que lo
utiliza y sustituir la herencia por composición

### Ejemplo 1
**Situacion y problema**: Tenés un algoritmo que varía según el contexto (por ejemplo, distintos métodos de pago o rutas de envío), pero el código está lleno de condicionales (if, switch) que dificultan el mantenimiento y la extensión.

**Solucion**: El patrón Strategy permite definir una familia de algoritmos, encapsular cada uno en su propia clase e intercambiarlos fácilmente en tiempo de ejecución. 

**En codigo**:
- **Strategy**
```
interface MetodoPago {
    void pagar(double monto);
}
```
- **ConcreteStrategies**
```
class PagoConTarjeta implements MetodoPago {
    public void pagar(double monto) {
        System.out.println("Pagando $" + monto + " con tarjeta.");
    }
}

class PagoConPaypal implements MetodoPago {
    public void pagar(double monto) {
        System.out.println("Pagando $" + monto + " con PayPal.");
    }
}
```
- **Context**
```
class Carrito {
    private MetodoPago metodo;

    public Carrito(MetodoPago m) {
        metodo = m;
    }

    public void setMetodo(MetodoPago m) {
        metodo = m;
    }

    public void procesarPago(double monto) {
        metodo.pagar(monto);
    }
}
```
- **Client**
```
public class Main {
    public static void main(String[] args) {
        Carrito carrito = new Carrito(new PagoConTarjeta());
        carrito.procesarPago(100);

        carrito.setMetodo(new PagoConPaypal());
        carrito.procesarPago(200);
    }
}
```


## State
Permite a un objeto alterar su comportamiento cuando su estado interno cambia.

**Aplicabilidad**:
- Cuando el comportamiento de un objeto dependa de su estado y deba cambiar en tiempo de ejecución dependiendo de ese estado.
- Cuando las operaciones tengan largas sentencias condicionales con múltiples ramas que dependen del estado del objeto. <br>
Este estado se suele representar por una o más constantes enumeradas. Muchas veces son varias las operaciones que contienen esta misma estructura condicional. El patrón State sugiere crear nuevas clases para todos los estados posibles de un objeto, extrayendo todos los comportamientos específicos del estado para colocarlos dentro de esas clases.

### Estructura

![image](https://github.com/user-attachments/assets/736939af-c11b-47e4-92ac-a6e47d1e377c)

- La clase **Context** almacena una referencia a uno de los objetos de estado concreto y le delega todo el trabajo específico del estado. El contexto se comunica con el objeto de estado a través de la interfaz de estado. El contexto expone un modificador (setter) para pasarle un nuevo objeto de estado.
- La interfaz **State** declara los métodos específicos del estado. Estos métodos deben tener sentido para todos los estados concretos, porque no querrás que uno de tus estados tenga métodos inútiles que nunca son invocados.
- Los **ConcreteStates** proporcionan sus propias implementaciones para los métodos específicos del estado.
- Tanto el estado de contexto como el concreto pueden establecer el nuevo estado del contexto y realizar la transición de estado sustituyendo el objeto de estado vinculado al contexto.

*Efectos deseados*: El patrón sigue el Principio de Responsabilidad Única (organiza en clases separadas el código relacionado con estados particulares) y el Principio Abierto/Cerrado (es posible introducir nuevos estados sin cambiar las clases de estado existentes o la clase contexto).

### Ejemplo 1
**Situacion**:  Estás desarrollando una aplicación para cajeros automáticos. El cajero puede estar en diferentes estados:
- Sin tarjeta insertada.
- Tarjeta insertada pero sin PIN.
- PIN validado y listo para operar.<br>
Dependiendo del estado, las acciones del usuario (insertar tarjeta, ingresar PIN, extraer dinero) tienen comportamientos distintos.

**Problema**: Si se implementa todo en una sola clase con condicionales
```
if (estado == "TARJETA_INSERTADA") {
    // hacer esto
} else if (estado == "PIN_VALIDO") {
    // hacer otra cosa
}
```
El código se vuelve largo, enredado y difícil de mantener, y agregar un nuevo estado requiere modificar muchas partes del código.

**Solucion**: El patrón State sugiere mover el comportamiento específico de cada estado a clases separadas. El objeto principal (Cajero) delega su comportamiento al objeto de estado actua:
- Cada estado es una clase que implementa la misma interfaz de estado
- El contexto (Cajero) mantiene una referencia al estado actual.
- Cuando se realiza una acción (como insertarTarjeta()), el cajero simplemente delegará al estado actual.

**En codigo**:
- **State**
```
public interface EstadoCajero {
    void insertarTarjeta();
    void ingresarPin();
    void extraerDinero();
}
```
- **Contexto**
```
public class Cajero {
    private EstadoCajero estadoActual;

    public Cajero() {
        this.estadoActual = new EstadoSinTarjeta(this);
    }

    public void setEstado(EstadoCajero estado) {
        this.estadoActual = estado;
    }

    // Métodos delegados
    public void insertarTarjeta() {
        estadoActual.insertarTarjeta();
    }

    public void ingresarPin() {
        estadoActual.ingresarPin();
    }

    public void extraerDinero() {
        estadoActual.extraerDinero();
    }
}
```
- **ConcreteStates**
```
class SinTarjeta implements Estado {
    Cajero cajero;

    SinTarjeta(Cajero c) { cajero = c; }

    public void insertarTarjeta() {
        System.out.println("Tarjeta insertada");
        cajero.setEstado(new ConTarjeta(cajero));
    }

    public void ingresarPin() {
        System.out.println("Inserte tarjeta primero");
    }

    public void extraer() {
        System.out.println("Sin tarjeta");
    }
}
```

```
class ConTarjeta implements Estado {
    Cajero cajero;

    ConTarjeta(Cajero c) { cajero = c; }

    public void insertarTarjeta() {
        System.out.println("Ya hay tarjeta");
    }

    public void ingresarPin() {
        System.out.println("PIN correcto");
        cajero.setEstado(new Autenticado(cajero));
    }

    public void extraer() {
        System.out.println("Ingrese PIN primero");
    }
}
```

```
class Autenticado implements Estado {
    Cajero cajero;

    Autenticado(Cajero c) { cajero = c; }

    public void insertarTarjeta() {
        System.out.println("Ya hay tarjeta");
    }

    public void ingresarPin() {
        System.out.println("PIN ya ingresado");
    }

    public void extraer() {
        System.out.println("Dinero entregado");
        cajero.setEstado(new SinTarjeta(cajero));
    }
}
```

- **Client**
```
public class Main {
    public static void main(String[] args) {
        Cajero c = new Cajero();
        c.insertarTarjeta();
        c.ingresarPin();
        c.extraer();
    }
}
```

### State vs Strategy
![image](https://github.com/user-attachments/assets/9edc8025-7048-41ce-affb-4b027f46d378)

## Template Method
Define en una operación el esqueleto de un algoritmo, delegando en las subclases algunos de sus pasos. Permite que las subclases redefinan ciertos pasos del algoritmo sin cambiar su estructura

El patrón Template Method sugiere que dividas un algoritmo en una serie de pasos, conviertas estos pasos en métodos y coloques una serie de llamadas a esos métodos dentro de un único método plantilla. Los pasos pueden ser abstractos, o contar con una implementación por defecto. Para utilizar el algoritmo, el cliente debe aportar su propia subclase, implementar todos los pasos abstractos y sobrescribir algunos de los opcionales si es necesario

**Aplicabilidad**:
- Cuando se desee implementar en una clase las partes de un algoritmo que no cambian y dejar que sean las subclases quienes implementen el comportamiento que puede variar
- Cuando, para evitar el código duplicado, se desee localizar en una clase común el comportamiento repetido de varias subclases.

### Estructura

![image](https://github.com/user-attachments/assets/dc51c45c-d661-44d2-bc26-275c1cce93d1)

- La **AbstractClass** declara métodos que actúan como pasos de un algoritmo, así como el propio método plantilla que invoca estos métodos en un orden específico. Los pasos pueden declararse abstractos o contar con una implementación por defecto.
- Las **ConcreteClass** pueden sobrescribir todos los pasos, pero no el propio método plantilla.

*Efectos deseados*: El patrón permite a los clientes que sobrescriban tan solo ciertas partes de un algoritmo grande, para que les afecten menos los cambios que tienen lugar en otras partes del algoritmo, y sigue el Principio DRY al colocar el código duplicado dentro de una superclase. Los métodos plantilla son una técnica fundamental de reutilización de código

### Ejemplo 1
**Situacion**:Una aplicación prepara bebidas calientes. Existen muchas similitudes entre preparar té y preparar café: hervir agua, servir en taza... pero cada bebida tiene su preparación específica. Originalmente, cada clase implementa el proceso completo por separado,  lo que genera código duplicado y difícil de mantener.

**Problema**: Cuando varias clases siguen el mismo flujo de pasos pero difieren en algunos detalles, es común copiar y pegar la estructura del algoritmo. Esto viola el principio DRY y vuelve costoso aplicar cambios comunes, porque hay que modificarlos en todas las clases afectadas.

**Solucion**: El patrón Template Method propone definir el esqueleto del algoritmo en una clase base (abstracta), y permitir que las subclases redefinan solo los pasos que varían. Así, se mantiene centralizado el control del flujo, pero se delega la personalización.

**En codigo**:
- **AbstractClass**
```
abstract class Bebida {
    public final void preparar() {
        hervirAgua();
        prepararIngrediente(); // paso variable
        servir();
    }

    void hervirAgua() {
        System.out.println("Hirviendo agua");
    }

    abstract void prepararIngrediente();

    void servir() {
        System.out.println("Sirviendo en taza");
    }
}
```
- **ConcreteClass**
```
class Cafe extends Bebida {
    void prepararIngrediente() {
        System.out.println("Agregando café molido");
    }
}

class Te extends Bebida {
    void prepararIngrediente() {
        System.out.println("Agregando saquito de té");
    }
}
```
- **Client**
```
public class Main {
    public static void main(String[] args) {
        Bebida cafe = new Cafe();
        cafe.preparar();

        Bebida te = new Te();
        te.preparar();
    }
}
```

## Interpreter
El patrón Interpreter define una forma de evaluar sentencias de un lenguaje. Para ello, modela una gramática usando una jerarquía de clases, donde cada clase representa un símbolo de la gramática y sabe cómo interpretarse a sí misma.

En esencia, este patrón permite interpretar o evaluar expresiones siguiendo reglas definidas de forma flexible y extensible.

## Visitor
Representa una operación sobre los elementos de una estructura de objetos. Permite definir una nueva operación sin cambiar las clases de los elementos sobre los que opera.

El patrón Visitor sugiere que coloques el nuevo comportamiento en una clase separada llamada visitante, en lugar de intentar integrarlo dentro de clases existentes. El objeto que originalmente tenía que realizar el comportamiento se pasa ahora a uno de los métodos del visitante como argumento, de modo que el método accede a toda la información necesaria contenida dentro del objeto.

Se utiliza una técnica llamada **Double Dispatch**, que ayuda a ejecutar el método adecuado sobre un objeto sin complicados condicionales. En lugar de permitir al cliente seleccionar una versión adecuada del método a llamar, ¿qué tal si delegamos esta opción a los objetos que pasamos al visitante como argumento? Como estos objetos conocen sus propias clases, podrán elegir un método adecuado en el visitante más fácilmente. “Aceptan” un visitante y le dicen qué método visitante debe ejecutarse.

**Aplicabilidad**: 
- Cuando una estructura de objetos contiene muchas clases de objetos con diferentes interfaces, y se quiere realizar operaciones sobre esos elementos que dependen de su clase concreta.
- Cuando se necesita realizar muchas operaciones distintas y no relacionadas sobre objetos de una estructura de objetos, y se quiere evitar “contaminar” sus clases con dichas operaciones.
- Cuando las clases que definen la estructura de objetos rara vez cambian, pero se desea definir nuevas operaciones sobre la estructura.

### Estructura

![image](https://github.com/user-attachments/assets/4ccfc93b-533a-4035-b78f-b5538b3e3d58)

- La interfaz **Visitor** declara metodos visitantes que pueden tomar elementos concretos de una estructura de objetos como argumentos
- Cada **ConcreteVisitor** implementa varias versiones de los mismos comportamientos,  personalizadas para las distintas clases de **ConcreteElement**
- La interfaz **Element** declara un metodo para "aceptar" visitantes. Este método deberá contar con un parámetro declarado con el tipo de la interfaz visitante
- Cada **ConcreteElement** implementara el metodo de aceptacion (accept). El propósito de este método es redirigir la llamada al método adecuado del visitante correspondiente a la clase de elemento actual

*Efectos deseados*: El patrón sigue el Principio de Responsabilidad Única (es posible tomar varias versiones del mismo comportamiento y ponerlas en la misma clase) y el Principio Abierto/Cerrado (introducir un nuevo comportamiento que puede funcionar con objetos de clases diferentes sin cambiar esas clases).

### Ejemplo 1
**Situacion**: Tenés una jerarquía de clases (Circulo, Cuadrado, Triángulo) que representan diferentes figuras geométricas. Están bien encapsuladas y cada una tiene sus propios datos (como radio o lados).

Un día, necesitás calcular el área de cada figura. Otro día, necesitás generar una versión en texto de cada figura. Después querés guardar cada figura en disco.

Agregar estas operaciones directamente dentro de las clases haría que esas clases cambien constantemente. Y si las clases son parte de una librería que no podés modificar, se vuelve peor aún.

**Problema**: Querés realizar múltiples operaciones sobre objetos de una jerarquía, pero no querés (o no podés) modificar las clases de esos objetos cada vez que agregás una nueva operación. Además, estas operaciones pueden depender del tipo concreto del objeto (ej: calcular el área de un Círculo no es igual que en un Cuadrado).

**Solucion**: El patrón Visitor permite separar las operaciones de los objetos sobre los que operan. Para ello, cada clase de objeto acepta un "visitante" que tiene métodos especializados para operar con cada tipo de objeto.

**En codigo**
- **Element**
```
interface Figura {
    void aceptar(Visitante visitante);
}
```
- **ConcreteElement**
```
class Circulo implements Figura {
    int radio;

    public Circulo(int radio) {
        this.radio = radio;
    }

    public void aceptar(Visitante visitante) {
        visitante.visitar(this);
    }
}

class Cuadrado implements Figura {
    int lado;

    public Cuadrado(int lado) {
        this.lado = lado;
    }

    public void aceptar(Visitante visitante) {
        visitante.visitar(this);
    }
}
```
- **Visitor**
```
interface Visitante {
    void visitar(Circulo c);
    void visitar(Cuadrado s);
}
```
- **ConcreteVisitor**
```
class AreaVisitante implements Visitante {
    public void visitar(Circulo c) {
        System.out.println("Área del círculo: " + (Math.PI * c.radio * c.radio));
    }

    public void visitar(Cuadrado s) {
        System.out.println("Área del cuadrado: " + (s.lado * s.lado));
    }
}
```
- **Client**
```
public class Main {
    public static void main(String[] args) {
        Figura[] figuras = {
            new Circulo(5),
            new Cuadrado(4)
        };

        Visitante visitante = new AreaVisitante();

        for (Figura figura : figuras) {
            figura.aceptar(visitante);
        }
    }
}
```

Como funciona
```
Cliente:
    figura.aceptar(visitante)
        ↓
Circulo:
    visitante.visitar(this)
        ↓
AreaVisitante:
    visitar(Circulo c) → lógica de cálculo de área
```
El visitor se entera a que metodo ir porque se le pasa el this en visitante.visitar(**this**)

## Observer
Define una dependencia de uno-a-muchos entre objetos, de forma que cuando un objeto cambie de estado se notifica y se actualizan automáticamente todos los objetos que dependen de él.

**Aplicabilidad**:
- Cuando una abstracción tiene dos aspectos y uno depende del otro (encapsular estos aspectos en objetos separados permite modificarlos y reutilizarlos de forma independiente).
- Cuando un cambio en un objeto requiere cambiar otros, y no se sabe cuántos objetos necesitan cambiarse.
- Cuando un objeto debería ser capaz de notificar a otros sin hacer suposiciones sobre quiénes son dichos objetos (en otras palabras, cuando no se quiere que estos objetos estén fuertemente acoplados)

### Estructura
![image](https://github.com/user-attachments/assets/acea87f8-6060-44e7-8678-d42c1d4b652c)

- La interfaz **Subject** define la interfaz para los objetos observables (notificadores), mantiene una lista de objetos observadores (suscriptores)
- El **ConcreteSubject** es una clase que implementa Subject, es el notificador. Envía eventos de interés a otros objetos. Esos eventos ocurren cuando el notificador cambia su estado o ejecuta algunos comportamientos.
-  Cuando sucede un nuevo evento, el notificador recorre la lista de suscripción e invoca el método de notificación declarado en la interfaz **Observer** en cada objeto suscriptor.
-  La interfaz **Observer** declara la interfaz de notificación. En la mayoría de los casos, consiste en un único método actualizar (update)
-  Los **ConcreteObservers** realizan algunas acciones en respuesta a las notificaciones emitidas por el notificador. Todas estas clases deben implementar la misma interfaz de forma que el notificador no esté acoplado a clases concretas.
-  El **Client** crea objetos tipo notificador y suscriptor por separado y después registra a los suscriptores para las actualizaciones del notificador.

*Efectos deseados*: El patrón sigue el Principio Abierto/Cerrado (el patrón permite agregar clases notificadoras Subject y clases suscriptoras Observer de forma independiente, siendo posible reutilizar las primeras sin reutilizar las segundas, y viceversa).

### Ejemplo 1
**Situacion**:Tenés una aplicación de noticias. Cuando se publica una nueva noticia, querés que distintos módulos reaccionen automáticamente: uno la guarda en base de datos, otro actualiza la interfaz, otro la envía por mail, etc.

Inicialmente, tenés que modificar la clase principal cada vez que querés agregar un nuevo módulo. Esto hace que el código sea frágil y muy acoplado.

**Problema**: El Subject (Publisher) necesita notificar a múltiples objetos cuando cambia, pero no debe conocer ni depender de las clases concretas que reaccionan. Agregar o quitar comportamiento obliga a modificar el código original del publisher

**Solucion**: El patrón Observer permite que múltiples objetos (Observers / Subscribers) se suscriban a eventos generados por un objeto central (Subject / Publisher). El Subject mantiene una lista de observadores y los notifica automáticamente cada vez que ocurre un evento, sin saber qué hacen.

**En codigo**
**Observer**
```
interface Subscriber {
    void update(String noticia);
}
```
**Subject**
```
interface Publisher {
    void agregar(Subscriber s);
    void quitar(Subscriber s);
    void notificar(String noticia);
}
```
**ConcreteSubject**
```
class Diario implements Publisher {
    private List<Subscriber> subs = new ArrayList<>();

    public void agregar(Subscriber s) { subs.add(s); }
    public void quitar(Subscriber s) { subs.remove(s); }

    public void publicarNoticia(String noticia) {
        System.out.println("Publicando: " + noticia);
        notificar(noticia);
    }

    public void notificar(String noticia) {
        for (Subscriber s : subs) {
            s.update(noticia);
        }
    }
}
```
**ConcreteObservers**
```
class AlertaEmail implements Subscriber {
    public void update(String noticia) {
        System.out.println("📧 Enviando email: " + noticia);
    }
}

class ActualizadorUI implements Subscriber {
    public void update(String noticia) {
        System.out.println("🖥️ Actualizando interfaz: " + noticia);
    }
}
```
**Client**
```
public class Main {
    public static void main(String[] args) {
        Diario diario = new Diario();

        Subscriber mail = new AlertaEmail();
        Subscriber ui = new ActualizadorUI();

        diario.agregar(mail);
        diario.agregar(ui);

        diario.publicarNoticia("Nueva edición disponible.");
    }
}
```



## Null object

<div style="page-break-after: always;"></div>

