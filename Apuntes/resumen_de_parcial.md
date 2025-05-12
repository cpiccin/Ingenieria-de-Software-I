# Entender el Problema

## Product discovery 
`_build the right thing_  ✅ ≠ _build the thing right_ ❌`

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
Se usa para mostrar cuánto trabajo queda por hacer a lo largo del tiempo en un sprint o proyecto.

En el eje horizontal (X) se representa el **tiempo**, normalmente dividido en días del sprint o semanas del proyecto.

En el eje vertical (Y) se muestra la cantidad de trabajo restante, que puede medirse en horas, tareas, puntos de historia, etc.

¿Cómo se interpreta?

- Al comienzo del sprint, se parte desde el total del trabajo estimado.
- A medida que se completan tareas, la línea desciende.
- Idealmente, la línea baja de manera constante hasta llegar a cero al final del sprint.
- Si la línea se mantiene plana o baja muy lentamente, puede indicar que el equipo está retrasado.


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
