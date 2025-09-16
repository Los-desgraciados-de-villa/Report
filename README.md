# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.
### 5.1.1. Software Development Environment Configuration.
### 5.1.2. Source Code Management.
### 5.1.3. Source Code Style Guide & Conventions.
A continuacióbn se explica e indica las referencias que se adoptaron para nombrar elementos y programar en los lenguajes que se han utilizado en esta solución.
#### HTML:
- Usar el correcto tipo de documento: Siempre se debe declarar el tipo de documento en la primera línea en el documento.
```html
<!DOCTYPE html>
```

- Usar nombres de elementos en minúsculas: El HTML5 permite mezclar letras mayúsculas y minúsculas en los nombres de elementos. Se recomienda usar nombres de elementos en minúsculas a razón de que en XHTML es requerido, es más fácil de escribir y luce más limpio.
```html
<section>
  <p>Esto es un párrafo.</p>
</section>
```

- Cerrar todos los elementos HTML: En HTML5, no es necesario cerrar todos los elementos, pero es recomendable cerrar todos los elementos.
```html
<!-- Válido pero no recomendado -->
<section>
 <p>Esto es un párrafo.
</section>

<!-- Válido y recomendado -->
<section>
  <p>Esto es un párrafo.</p>
</section>
```

- Cerrar todos los elementos HTML vacíos: En HTML5, es opcional cerrar los elementos vacíos pero es recomendable cerrarlos.
``` html
<!-- Permitido -->
<meta charset="utf-8">

<!-- Permito y recomendado -->
<meta charset="utf-8" />
```

- Usar nombres de atributos en minúsculas: HTML5 permite mezclar letras mayúsculas y minúsculas en los nombres de los atributos. Se recomienda usar letras minúsculas a razón de que en XHTML es requerido, es más fácil de escribir y luce más claro.
```html
<!-- Permitido pero no compatible con XML ni XHTML -->
<div CLASS="menu">

<!-- Recomendado y compatible con XML y XHTML -->
<div class="menu">
```

- Usar comillas en los valores de atributos: El HTML5 permite atributos sin comillas. Se recomienda el uso de comillas a razón de es más fácil de leer y debe usarse si el valor contiene espacios.
``` html
<!-- Esto no funciona porque el valor contiene espacios -->
<table class=table striped>

<!-- Funciona pero no es compatible con XML ni XHTML -->
<table class=striped>

<!-- Funciona y es compatible con XML y XHTML -->
<table class="striped">
```

- Usar atributos en Imágenes: Siempre agregara el atributo alt a las imágenes. El atributo es importante cuando la imagen por alguna razón no es mostrado. También, siempre el ancho y alto. Esto reduce el parpadeo porque el navegador puede reservar espacio para la imagen antes de cargarla.
``` html
<!-- Funciona pero no es recomendado -->
<img src="algo.gif">

<!-- Funciona y es lo recomendado -->
<img src="algo.gif" alt="HTML5" style="width: 128px; height: 128px;">
```

- Espacios y Signos de Igualdad: HTML5 permite los espacios alrededor de los signos igual (=), pero sin los espacios es más fácil de leer y agrupa mejor las entidades.
```html
<!-- Funciona pero es confuso para leer -->
<link rel = "stylesheet" href = "styles.css">

<!-- Funciona y es fácil de leer -->
<link rel="stylesheet" href="style.css">
```

#### CSS:
- Bloque (Block): El bloque encapsula una entidad independiente que es significativa por sí misma. Aunque los bloques se pueden anidar o interactuar, cada uno es independiente y tiene sentido por sí solo.
```css
.card { background-color: #eee; }
```

- Elemento (Element): Los elementos son parte de un bloque y, por lo tanto, dependen de este. Un ejemplo concreto podría ser un título para el bloque "card. La clase CSS se forma combinando el nombre del bloque con dos guiones bajos y el nombre del elemento:
```css
.card__title { color: #111; }
```

- Modificador (Modifier): Los modificadores son todos aquellas clases que modifican o agregan estilo a un bloque o elemento. La clase CSS se forma como el nombre del bloque o elemento más dos guiones.
```css
.card--dark { background-color: #111; }
```

#### JAVASCRIPT:
- Comillas: Hay algunas recomendaciones acerca de esta notación. Aunque Javascript permite usar comillas simples o comillas dobles indistintamente, generalmente es recomendable, en ciertos casos, escribir con comillas simples y en otros con comillas dobles.
```javascript
const foo =’”Bienvenidos”’; 
console.log(foo); // “Bienvenidos”
// 
const foo1 =”’Bienvenidos’”;
console.log(foo1); // ‘Bienvenidos’
//Otro ejemplo
const foo2 = ‘Bienvenidos,’;
const foo3 = ‘Hola’;
console.log(foo2 + foo3 + ‘ Mundo.’); //Bievenidos, Hola Mundo.
```

- Llaves: La llave de apertura deberá ir en la misma lí­nea de la sentencia. Si colocas en la siguiente lí­nea, en algunos casos muy particulares se puede producir algún error. Más adelante se explica dicho error en el uso de punto y coma en las sentencias.
```javascript
// control flow stament
if ( true ) {
 //codes goes here
}
//Anonymous function declaration
function ( args ) {
   return true;
}
//Named function declaration
function foo() {
   return true;
}
//Anonymous function expression
const bar = function ( args ) {
   return true;
}
//Arrow function
const bar = (arg) => {
   return true,
};
const bar = ( args ) => { true };
const bar = ( args ) => true;
```

- Punto y coma: Javascript utiliza ASI (Automatic Semicolon Insertion) cuando se trata de insertar un “punto y coma” que ha sido omitido en cada instrucción , y que es separada en una lí­nea diferente. Técnicamente es posible, sin embargo esta no es una buena práctica, porque en ciertas ocasiones se puede generar un error que será un quebradero de cabeza poder solucionarlo.
```javascript
console.log(getName());
function getName(){
   return 
   {
     name: ‘@davidenq’
   }
}
```

### 5.1.4. Software Deployment Configuration.
Para lograr el correcto deployado de la Landing Page desarrollada se siguieron los siguientes pasos:

- En la organización del grupo se creó un repositorio exclusivamente para subir y deployar la Landing Page.
<img width="1902" height="947" alt="image" src="https://github.com/user-attachments/assets/743bac1f-31e1-420c-830b-9fa16960f59a" />


## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1.
En esta sección se da a conocer el planeamiento que se ha tenido para el desarrollo e implementación inicial del proyecto "Nombre". En este enfoque se priorizó el desarrollo inicial de dicho proyecto, la implementación de la Landing Page la cual fue fundamental para poder dar a conocer la Startup y convencer al usuario, esta se muestra de manera clara, usable y ágil para el usuario final.

#### 5.2.1.2. Aspect Leaders and Collaborators.
#### 5.2.1.3. Sprint Backlog 1.
Durante Sprint 1 se desarrollaron funcionalidades fundamentales para facilitar la experiencia del usuario al navegar, se priorizó que esta sea fácil, amigable y visualmente adaptable al usuario. Detallamos a continuación las tareas asocidadas a las historias de usuario que se han priorizado desarrollar para este Spring.

#### 5.2.1.4. Development Evidence for Sprint Review.
#### 5.2.1.5. Execution Evidence for Sprint Review.
#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review.
#### 5.2.1.8. Team Collaboration Insights during Sprint.

## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.
### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.

## 5.4. Video About-the-Product.
