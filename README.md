# bitacora-html
## ¿Actividad Página estatica en HTML Bitacoras?

Este repositorio es para el programa de Análisis y Desarrollo de Software (ADSO) del SENA. Básicamente hicimos una estatica empleando solo html, sin css ni javascript, con el fin de visualizar las bitacoras del lider del grupo 7 de trabajo, en dichas bitacoras se registran sus actividades diarias de aprendizaje.

La idea es que la pagina sea como un control de trabajo diario donde se documenta lo que se hace en cada sesión de clase. El sitio tiene varias páginas que están conectadas entre sí para poder navegar fácilmente.

---

## Estructura de archivos

Así quedó organizado el repositorio:

```
bitacora-html/
├── README.md              # Este archivo
├── TEAM_AGREEMENT.md      # Acuerdo del equipo
├── index.html             # Página de documentación y desarrollo del proyecto
├── formulario.html        # Página de formulario
├── informacion.html       # Página de información
├── reglas.html            # Página de reglas
├── trazabilidad.html      # Índice de bitácoras
└── bitacoras/             # Carpeta con las bitácoras por día
    ├── dia1.html          # Semana 2, día 1
    ├── dia2.html          # Semana 2, día 2
    ├── dia3.html          # Semana 3, día 3
    ├── dia4.html          # Semana 4, día 1
    ├── dia5.html          # Semana 4, día 2
    ├── dia6.html          # Agosto semana 5 (bitácora extra del mes)
    └── dia7.html          # Septiembre semana 1
```

---

## Las tres vistas que desarrollamos

### 1. index.html - El formulario

Esta es la página principal. Tiene un formulario donde el aprendiz pone sus datos antes de entrar a la bitácora. Los campos que tiene son: nombre, apellido, teléfono, ciudad y género.

Lo que usamos aquí:
- Un `<form>` que manda a informacion.html cuando le das enviar
- Cada campo tiene su `<label>` conectado con el input usando el atributo `for` y `id`
- El teléfono es tipo `number` y tiene un select para elegir la ciudad (Bucaramanga, Floridablanca o Girón)
- Para el género usamos radio buttons
- Los campos de nombre y apellido tienen `required` para que sean obligatorios

En cuanto a accesibilidad y semántica:
- Pusimos `<!DOCTYPE html>` al inicio del documento
- El `<html lang="es">` para decir que está en español
- El meta charset UTF-8 para que se vean bien las tildes y la ñ
- El meta viewport para que se vea bien en el celular
- Los labels están bien asociados a los inputs, eso es importante para los lectores de pantalla
- El formulario usa `action` y `method` que es lo correcto

---

### 2. informacion.html - Información del programa

Aquí va la información general del programa. Muestra cosas como la versión, la competencia, el número de ficha, el nombre del autor y el sprint en el que estamos.

Lo que tiene:
- Un menú arriba con enlaces para ir a las otras páginas (Información, Reglas y Bitácoras)
- Una tabla con los datos del programa de formación
- Un botón para volver al formulario
- Los títulos con h1 y h2

Sobre accesibilidad y semántica:
- También tiene `<html lang="es">` y el charset UTF-8
- Usamos h1 y h2 para que haya un orden en los títulos, primero el principal y luego los secundarios
- La tabla es semántica, o sea que es una `<table>` como debe ser para mostrar datos
- Los enlaces tienen texto que dice a dónde van, no pusimos cosas como "click aquí"
- El title de la página dice "Información - Bitácora ADSO" para que se sepa de qué trata
- El menú de navegación es igual en todas las páginas para que sea consistente

---

### 3. reglas.html - Reglas y guía de llenado

Esta página es para explicar cómo se debe usar la bitácora. Tiene las reglas que hay que seguir y una guía de cómo llenar cada columna de la tabla de trazabilidad.

Lo que incluye:
- Una lista ordenada con `<ol>` que tiene 4 reglas principales (como lo de la responsabilidad única, no poner adjetivos subjetivos, etc.)
- Los nombres de las reglas están en negrita con `<strong>` para que resalten
- Una tabla grande que explica qué va en cada columna (ID, Timestamp, Autoría, etc.)
- El mismo menú de navegación que las otras páginas

En lo de accesibilidad y semántica:
- Lo mismo que las otras páginas: lang="es", charset UTF-8
- Los títulos están bien organizados con h1 y h2
- Usamos `<ol>` porque las reglas van numeradas, si fueran sin orden usaríamos `<ul>`
- El `<strong>` es para darle importancia semántica a los nombres de las reglas, no es solo para poner negrita
- La tabla tiene `<thead>` para los encabezados y `<tbody>` para el contenido, eso es buena práctica
- Todo el texto es claro y explica bien qué hay que hacer

---

## La página de trazabilidad

También tenemos el archivo `trazabilidad.html` que es como el índice de todas las bitácoras. Ahí hay una tabla organizada por semanas donde puedes hacer clic en cada día para ver la bitácora correspondiente.

Lo que tiene:
- Una tabla con `rowspan` para agrupar los días por semana
- Los enlaces tienen `target="visor"` para que se abran en un visor
- Las filas tienen colores alternados para que sea más fácil de leer
- El menú de navegación igual que en las otras páginas

Sobre accesibilidad:
- Tiene lang="es" y charset UTF-8 como las demás
- La tabla usa `<thead>` y `<tbody>`
- El `rowspan` ayuda a agrupar visualmente los datos relacionados
- Los enlaces dicen "Ver Bitácora" que es más descriptivo que solo "click aquí"
- Usa `bgcolor` para diferenciar las filas visualmente

---

## Resumen de lo que hicimos con accesibilidad y semántica

En todos los archivos HTML pusimos:
- `<!DOCTYPE html>` al inicio
- `<html lang="es">` para el idioma
- `<meta charset="UTF-8">` para los caracteres

En index.html específicamente:
- El meta viewport para responsividad
- Labels asociados a inputs con for/id
- Validación con required
- El formulario con action y method

En informacion.html, reglas.html y trazabilidad.html:
- Jerarquía de títulos con h1 y h2
- Tablas semánticas con thead y tbody
- Navegación consistente entre páginas
- Títulos descriptivos en el tag title

En reglas.html además:
- Lista ordenada con `<ol>`
- Uso de `<strong>` para énfasis semántico

---

## El equipo

Somos tres personas trabajando en esto:
- David Santiago Santos Amaya - Líder (Arquitecto) - @David-santiago-svg
- Nataly Velasco Navarro - Desarrollador - @NatalyNavarro
- Manuel Fernando Paredes - Desarrollador - @ManuelFernando95

---

## Tecnologías que usamos

- HTML5 para la estructura
- Git y GitHub para el control de versiones
- Git Flow para trabajar en equipo con ramas

---

## Convenciones de commits

Para los commits usamos:
- `feat:` cuando es una nueva funcionalidad
- `docs:` cuando es documentación
- `fix:` cuando es una corrección

---

*Este README es parte de la actividad de la ficha 3533582 - ADSO, SENA*