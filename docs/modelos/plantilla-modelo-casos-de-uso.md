# Plantilla del modelo de casos de uso de Proyecto Simbiosis

| Versión | Fecha | Estado |
| --- | --- | --- |
| 1.7 | 20/10/2026 | Plantilla |

Esta es la plantilla base reutilizable. Conserva sus instrucciones y campos pendientes. Para iniciar el modelo, copia su contenido en [modelo-casos-de-uso.md](modelo-casos-de-uso.md). Si el modelo ya contiene resultados, continúa sobre él sin sustituirlos por la plantilla.

**Iteración de referencia:** [Indica la última iteración incorporada al modelo.]

Este documento recoge el modelo de casos de uso del proyecto. Se completa a medida que se incorporan funciones. Los diagramas muestran distintas vistas del mismo modelo.

Sustituye las indicaciones entre corchetes por tu contenido. Añade filas cuando las necesites. Si un apartado aún no se ha trabajado, indica que está pendiente. No inventes respuestas para completar la plantilla.

**Trabajo en E1.** El producto principal es el diagrama de la primera vista. Usa las funciones del apartado 4 del [plan de E1](../planificacion/plan-iteracion-e1.md). La anotación de alcance puede ser breve. Los apartados siguientes permiten organizar el modelo y continuarlo después. No se requieren descripciones detalladas de los casos en E1 ni se establece una entrega adicional.

**Evolución del documento.** Mantén `modelo-casos-de-uso.md` al avanzar de iteración. Conserva los identificadores de los elementos que sigan siendo los mismos. Actualiza los datos iniciales cuando registres una nueva versión del modelo. Cambia el estado de «Plantilla» a «Borrador» al empezar a completarlo. Usa «Revisado» solo después de la revisión correspondiente. Git conservará los estados registrados en commits.

## 1 Alcance del modelo

Explica qué funcionalidad representa el modelo en su estado actual. Indica qué funciones quedan pendientes. En E1, remite al plan para situar el alcance. No copies el catálogo completo.

[Explica el alcance actual y sus límites.]

En iteraciones posteriores, actualiza el alcance acumulado. Distingue las funciones nuevas de las que ya estaban representadas. Una vista puede cubrir solo una parte de un UR o de un módulo.

## 2 Actores

Registra los roles externos que participan en las funciones representadas. Un actor puede ser una persona o un sistema externo. Describe cada rol con una frase breve. No confundas estos roles con las personas del equipo de desarrollo.

| Nombre del actor | Rol que representa |
| --- | --- |
| [Nombre] | [Describe el rol externo.] |

Mantén los mismos nombres en las tablas, los diagramas y las descripciones.

[Si existen generalizaciones, identifica el actor general y los actores especializados. Explica qué relación existe entre ellos. Puedes hacer referencia a un diagrama adicional de actores si facilita la lectura. Si no utilizas generalizaciones, indícalo.]

## 3 Casos de uso

Registra los casos que aparecen en el modelo. Asigna a cada caso un identificador estable. Escribe el nombre con un verbo y un objeto. Resume el objetivo sin describir todos sus pasos.

| Identificador | Nombre | Objetivo | Participantes |
| --- | --- | --- | --- |
| [UC-…] | [Nombre] | [Explica el objetivo.] | [Indica los actores que participan.] |

[Indica los actores que participan. Si procede, distingue el actor principal, que busca alcanzar el objetivo del caso de uso y normalmente inicia la interacción, de los actores de apoyo, que proporcionan servicios o información al sistema.]

Esta distinción se establece para cada caso de uso. Un mismo actor puede desempeñar funciones diferentes en distintos casos. No es necesario asignar un actor principal independiente a cada caso incluido.

Al ampliar el modelo, conserva los casos anteriores que sigan siendo válidos. Si revisas un caso, conserva su identificador cuando siga representando el mismo objetivo. No reutilices el identificador de un caso retirado para un caso diferente.

## 4 Diagramas del modelo

Añade la primera vista en E1. En iteraciones posteriores, incorpora las vistas necesarias y revisa las anteriores cuando cambien elementos compartidos.

Para cada vista, incluye un título, una frase sobre su alcance y el diagrama. Todas las vistas deben usar la misma frontera del sistema y nombres compatibles.

### 4.1 Primera vista

**Título:** [Indica el título de la vista.]

**Alcance:** [Explica qué funciones representa esta vista.]

[Inserta aquí el diagrama.]

Si una decisión necesita aclaración, puedes añadir una nota breve junto al diagrama.

**Nombre y ubicación de la imagen.** Guarda las imágenes en `docs/modelos/imagenes/`. Usa este patrón:

```text
tipo-de-diagrama-ambito.png
```

El tipo indica qué diagrama contiene la imagen. El ámbito indica qué funciones o elementos representa. Usa minúsculas, sin tildes, eñes ni espacios, y separa las palabras con guiones.

Para la primera vista de E1, utiliza este nombre común:

```text
casos-de-uso-acceso-cuentas-ayuda-e1.png
```

Inserta la imagen con este enlace relativo:

```markdown
![Casos de uso de acceso cuentas y ayuda](imagenes/casos-de-uso-acceso-cuentas-ayuda-e1.png)
```

Al revisar esta vista, conserva el nombre del archivo y actualiza la imagen. Conserva el sufijo `-e1` de esta vista. La vista de salud y recetas de E2 utilizará `casos-de-uso-salud-recetas-e2.png`. No añadas la versión, la fecha ni tu nombre al archivo. Git conservará las versiones registradas en commits.

Si añades una vista diferente, utiliza otro ámbito. Si necesitas varias imágenes del mismo ámbito, añade un detalle que las distinga. La [guía de modelos](README.md) recoge los ejemplos y la convención que se ampliará para otros tipos de diagramas.

Conserva también el archivo editable de la herramienta cuando esté disponible. Usa el mismo nombre base y la extensión propia de la herramienta. Al revisar una vista, actualiza su imagen y su explicación. Las versiones anteriores quedarán en los commits que incluyan esos archivos.

## 5 Respaldo en los requisitos

Indica los UR y FR que respaldan las decisiones del modelo. Añade los NFR que condicionen un caso o su descripción. Explica la relación cuando el identificador no baste para comprenderla.

En E1 basta con un respaldo breve del diagrama. La tabla permite ampliar la trazabilidad después. No es necesario crear un caso independiente para cada FR o NFR.

| Elemento del modelo | UR y FR de referencia | NFR pertinentes | Relación con los requisitos |
| --- | --- | --- | --- |
| [Caso, actor o relación] | [Identificadores] | [Identificadores, si procede] | [Explica qué respaldan o condicionan.] |

Consulta el [catálogo canónico](../requisitos/catalogo-requisitos.md) y la [SRS](../requisitos/srs.md). Si falta una condición, indica que está pendiente de aclaración. No la presentes como un requisito confirmado.

## 6 Descripciones de los casos de uso

**Desarrollo posterior.** Este apartado queda pendiente en E1. Se completará cuando se trabajen las descripciones de los casos de uso. La existencia de este apartado no exige describirlos ahora.

Repite el esquema siguiente para cada caso que se vaya a describir. Sustituye `UC-XX` y el nombre del encabezado por el identificador y el nombre del apartado 3; numera los apartados de forma consecutiva. El nivel de detalle dependerá del trabajo previsto para ese caso.

### 6.1 Descripción detallada UC-XX — Actualizar perfil

**Identificador y nombre del caso de uso:** Actualizar perfil (UC-05)

**Objetivo:** Modificar los datos personales y conservar los cambios.

**Participantes:** Usuario registrado.

**Precondiciones:** La persona ya tiene una cuenta activa y una sesión iniciada.

**Inicio:** El usuario solicita actualizar su perfil.

**Escenario principal de éxito:**
  - El sistema muestra los datos actuales indicando cuales son editables y cuales no editables.
  - El usuario modifica los campos de su perfil.
  - El usuario solicita guardar los cambios.
  - El sistema comprueba los datos se han introducido correctamente.
  - El sistema guarda los datos validados
  - El sistema confirma la modificación del perfil.
  - El caso de uso finaliza.

**Extensiones (flujos alternativos):**
  - 5.a faltan datos o hay datos no válidos.
  - *.a El usuario cancela en cualquier momento.

**Postcondiciones:** una vez finalizado el caso de uso con éxito se mantienen los datos actualizados, en caso de que falle o haya algún error se recuperan los daos originales y no se modifica nada.

**Reglas y NFR pertinentes:**
  - NFR-001 (NFR-Q · Disponibilidad): La plataforma alcanzará una disponibilidad mínima del 99,5 % en cada mes natural, medida mediante comprobaciones externas cada cinco minutos.
  - NFR-004(NFR-Q · Capacidad y escalabilidad): La plataforma soportará una carga de 100 usuarios concurrentes y 10 operaciones por segundo durante 30 minutos.
  - NFR-005 (NFR-Q · Rendimiento): Con la carga de NFR-004, el 95 % de los inicios de sesión y de las consultas definidas para la prueba se completará en un máximo de 2 segundos.
  - NFR-008 (NFR-Q · Recuperabilidad): Tras un incidente grave, la plataforma recuperará las funciones principales en un máximo de cuatro horas desde la declaración del incidente.
  - NFR-009 (NFR-Q · Integridad): Tras un incidente grave, la pérdida de información no superará la correspondiente a las 24 horas anteriores al incidente.
  - NFR-015 (NFR-I · Interfaz de software y autenticación): La autenticación mediante una cuenta de Google utilizará OAuth 2.0 u OpenID Connect sobre HTTPS y la plataforma no almacenará la contraseña de Google.
  - Tratamiento de datos de salud - El sistema no debe tratar esos datos hasta que esa decisión esté aprobada por la organización.

**Preguntas abiertas:** No hay preguntas

Describe el comportamiento que se necesita. Las decisiones sobre componentes, clases o tecnologías pertenecen al trabajo de arquitectura y diseño.

### 6.2 Descripción detallada UC-XX — Buscar recetas

**Identificador y nombre del caso de uso:** Buscar recetas (UC-21)

**Objetivo:** Consultar la información de una receta

**Participantes:** Usuario registrado.

**Precondiciones:** El usuario debe tener al menos una receta creada.

**Inicio:** El usuario pone en el buscador la información necesaria para buscar una receta.

**Escenario principal de éxito:**
  - El sistema encuentra la receta solicitada por el usuario.
  - El sistema valida que se ha encontrado la receta correcta.
  - El sitema muestra los datos de la receta.
  - El sistema detalla la información que requiera el usuario.
  - El caso de uso finaliza.

**Extensiones (flujos alternativos):**
  - 1.a. El usuario cancela la búsqueda.
  - 2.a. Faltan datos en la receta obtenida.
  - 2.b. El sistema muestra la receta errónea.

**Postcondiciones:** No se modifica ningun dato ni receta una vez finalizado el caso de uso.

**Reglas y NFR pertinentes:** 
  - NFR-002 (NFR-I · Integridad): La plataforma realizará al menos una copia de seguridad diaria de la información de salud y de las recetas.
  - NFR-006 (NFR-Q · Rendimiento): Con la carga de NFR-004, el 95 % de las publicaciones de recetas, comentarios o mensajes se completará en un máximo de 3 segundos.
  - NFR-008 (NFR-Q · Recuperabilidad): Tras un incidente grave, la plataforma recuperará las funciones principales en un máximo de cuatro horas desde la declaración del incidente.
  - NFR-009 (NFR-Q · Integridad): Tras un incidente grave, la pérdida de información no superará la correspondiente a las 24 horas anteriores al incidente.
  - Tratamiento de datos de salud - El sistema no debe tratar esos datos hasta que esa decisión esté aprobada por la organización.
  - Finalidad, minimización y conservación - El sistema solo debe recoger los datos necesarios para una finalidad definida. La organización debe establecer cuánto tiempo se conservan y cuándo se eliminan o anonimizan.
  - Información y derechos de las personas - El sistema debe informar de forma clara antes de recoger los datos sobre quién los trata, para qué y cómo pueden las personas ejercer sus derechos.

**Preguntas abiertas:** No hay preguntas
Describe el comportamiento que se necesita. Las decisiones sobre componentes, clases o tecnologías pertenecen al trabajo de arquitectura y diseño.

## 7 Continuidad entre iteraciones

En E1, indica que esta es la primera vista del modelo. A partir de la siguiente iteración, resume qué elementos se incorporan y cuáles se revisan, conservan o retiran.

Descripción de los casos de uso UC-05 y UC-21.

Este apartado describe la evolución del modelo. No sustituye la evaluación de la iteración. Los resultados de arquitectura, las pruebas y las desviaciones del plan se registran en sus documentos correspondientes.

El historial completo de este archivo está en Git. Para localizar el estado de cierre de una iteración, utiliza el commit identificado al cerrar esa iteración. La [guía de esta carpeta](README.md) explica el procedimiento.
