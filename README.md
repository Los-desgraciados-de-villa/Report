# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.
### 5.1.1. Software Development Environment Configuration.
### 5.1.2. Source Code Management.
### 5.1.3. Source Code Style Guide & Conventions.
A continuación se detallan las convenciones y guías de estilo adoptadas para el desarrollo del proyecto, siguiendo lineamientos internacionales y buenas prácticas de codificación. Se ha definido que toda la nomenclatura será escrita en **inglés**, independientemente del lenguaje utilizado.  
Las referencias consideradas incluyen: *Google HTML/CSS Style Guide, MDN JavaScript Guidelines, W3C JavaScript Style Guide, Vue.js Style Guide, C# Coding Conventions y Microsoft ASP.NET Core Coding Guidelines*.  

El proyecto se desarrollará en tres entornos principales:  
- **Visual Studio Code** para la Landing Page (HTML, CSS y JavaScript).  
- **WebStorm** para el frontend en **Vue.js**.  
- **JetBrains Rider** para el backend en **C# con .NET Core**.    

#### HTML:
- **Declarar el tipo de documento** en la primera línea:
```html
<!DOCTYPE html>
```

- **Usar etiquetas en minúscula** para consistencia y compatibilidad con XHTML:
```html
<section>
  <p>Esto es un párrafo.</p>
</section>
```

- **Cerrar todas las etiquetas**, incluso si HTML5 lo permite opcionalmente.
- **Atributos en minúscula** y siempre entre **comillas dobles**:
```html
<div class="menu"></div>
```

- **Incluir** alt **en imágenes** y definir "width" y "height" para optimizar el renderizado:
```html
<img src="logo.png" alt="Company Logo" width="128" height="128" />
```

- **Evitar espacios innecesarios en los atributos**:
```html
<link rel="stylesheet" href="style.css" />
```

#### CSS:
Se adoptará la metodología **BEM (Block, Element, Modifier)** para nombrar clases.
- **Block**: entidad independiente.
```css
.card { background-color: #eee; }
```

- **Element**: parte de un bloque, se nombra con __.
```css
.card__title { color: #111; }
```

- **Modifier**: variación de un bloque o elemento, se nombra con --.
```css
.card--dark { background-color: #111; }
```

#### JAVASCRIPT (incluye Vue.js):
- **Comillas**: se recomienda usar comillas simples ' ' por consistencia, salvo en strings que requieran escapar apóstrofes.
```javascript
const greeting = 'Hello World';
```

- **Llaves**: la llave de apertura va en la misma línea de la sentencia.
```javascript
if (true) {
  console.log('Valid');
}
```

- **Punto y coma**: obligatorio al final de cada sentencia para evitar errores por ASI (Automatic Semicolon Insertion).
```javascript
console.log(getName());

function getName() {
  return {
    name: 'User'
  };
}
```

- **Funciones**: preferir funciones flecha para callbacks y funciones anónimas.
```javascript
const sum = (a, b) => a + b;
```

- **Vue.js**:
  + Componentes nombrados en **PascalCase**.
  + Props en **camelCase** en el código, pero en **kebab-case** en el template.
  + Archivos ".vue" organizados en **template**, **script** y **style** en ese orden.
  + Un componente por archivo.

#### C#:
- **Convenciones de nombres**:
  + Clases y métodos PascalCase.
  + Variables y parámetros en camelCase.
  + Constantes en UPPER_CASE.
- **Estructura de llaves**: siempre en la siguiente línea para mayor legibilidad.
```csharp
  public class Property
{
    public string Address { get; set; }
}
```
- **Usar** "var" solo cuando el tipo es obvio por el lado derecho.
- **Manejo de excepciones**: usar "try/catch" únicamente cuando sea necesario y no abusar del control de flujo con excepciones.
- **Buenas prácticas en ASP.NET Core**:
  + Usar **Dependency Injection**.
  + Separar controladores, servicios y repositorios en carpetas organizadas.
  + Nombrar endpoints REST siguiendo convención **plural y en minúsculas** (/api/properties).

### 5.1.4. Software Deployment Configuration.
Para el despliegue de la solución, se definió la siguiente configuración y flujo:

**1. Repositorio en GitHub**:
- Se creó un repositorio exclusivo para la aplicación, donde se almacena el código fuente.
- Se adoptó la estrategia de branching con ramas principales (main) y ramas de desarrollo (feature/*).

**2. Automatización del despliegue:**:
- Se configuró *GitHub Pages* para la publicación de la Landing Page desarrollada en **Visual Studio Code**.
- Se considera la integración de *CI/CD* mediante **GitHub Actions** para desplegar el frontend en Vue.js (WebStorm) y el backend en .NET Core (Rider) hacia un servicio en la nube como **Azure App Service** o **AWS Elastic Beanstalk**.

**3. Pasos para despliegue manual de la Landing Page:**:
- **git clone <repo_url>** para clonar el proyecto.
- **git checkout main** para ubicar la rama principal.
- Subir cambios y ejecutar el flujo de publicación en GitHub Pages.

**4. Entorno de ejecución:**:
- **Cliente**: Navegadores modernos con soporte HTML5, CSS3 y ES6+.
- **Frontend**: Vue.js ejecutado en Node.js LTS.
- **Backend**: ASP.NET Core ejecutado en .NET 7.0+.
- **Base de datos**: SQL Server.

**5. Verificación del despliegue:**:
- Pruebas de accesibilidad y compatibilidad en la Landing Page.
- Validación de certificados SSL en el entorno desplegado.
- Prueba de rutas y endpoints en el frontend y backend.
- Validación de integración con la base de datos.


## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1.
En esta sección se da a conocer el planeamiento que se ha tenido para el desarrollo e implementación inicial del proyecto "Nombre". En este enfoque se priorizó el desarrollo inicial de dicho proyecto, la implementación de la Landing Page la cual fue fundamental para poder dar a conocer la Startup y convencer al usuario, esta se muestra de manera clara, usable y ágil para el usuario final.

#### 5.2.1.2. Aspect Leaders and Collaborators.
#### 5.2.1.3. Sprint Backlog 1.
Durante Sprint 1 se desarrollaron funcionalidades fundamentales para facilitar la experiencia del usuario al navegar, se priorizó que esta sea fácil, amigable y visualmente adaptable al usuario. Detallamos a continuación las tareas asocidadas a las historias de usuario que se han priorizado desarrollar para este Spring.

#### 5.2.1.4. Development Evidence for Sprint Review.
| Repository | Branch   | Commit Id | Commit Message | Commit Message Body | Commit on (Date) |
|-------------|----------|-----------|----------------------------------------------------------------|---------------------------------------------------------------|-------------------|
| [CertiInmueble](https://los-desgraciados-de-villa.github.io/Landing-page) | main  | c042919 | docs(assets): add company and logo picture | docs(assets): add company and logo picture | 15/09/2025 |
| [CertiInmueble](https://los-desgraciados-de-villa.github.io/Landing-page) | main  | 5dceb27  | feat(landing): add header section | feat(landing): add header section | 18/09/2025 |
| [CertiInmueble](https://los-desgraciados-de-villa.github.io/Landing-page) | main  | 49b9560  | feat(landing): add reviews section | feat(landing): add reviews section | 18/09/2025 |
| [CertiInmueble](https://los-desgraciados-de-villa.github.io/Landing-page) | main  | 8fd4024  | feat(landing): add contact and footer section | feat(landing): add contact and footer section | 19/09/2025 |
#### 5.2.1.5. Execution Evidence for Sprint Review.
Durante este primer Sprint, se implementó el diseño de la primera version del Landing Page, desplegado en Github Pages. A continuacion, se explicara las secciones importantes.

Sección Nosotros:
<img src=""/>

Sección Solocitar certificado:
<img src=""/>

Sección Servicios/Beneficios:
<img src=""/>

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
Para el Sprint 1, no se ha trabajado en la documentación de los servicios de la aplicación, ya que el enfoque principal ha sido la creación del Landing Page. Será durante los siguientes Sprints, donde se realizará el desarrollo de la documentación de los servicios

#### 5.2.1.7. Software Deployment Evidence for Sprint Review.
1. Creación de organización en Github.
<img src="https://github.com/user-attachments/assets/c2203281-366e-4880-a4b1-ad6329cf2ab0"/>

2. Asociación de los integrantes del equipo para la colaboración en los repositorios de la organización.
<img src="https://github.com/user-attachments/assets/72f918a5-e36e-4130-aa4f-7d2760306ac0"/>

3. Creación de repositorios separados para la organización de entregables
<img src="https://github.com/user-attachments/assets/9d8ef48c-384a-461e-9fe1-17d2ba1332e9"/>

4. Configuración y despliegue de la primera versión del Landing Page en **Github Pages**
<img src="https://github.com/user-attachments/assets/2ea31558-136a-434a-aa2f-fcd0a14ed8a1" />


#### 5.2.1.8. Team Collaboration Insights during Sprint.

Ahora, se mostraran las evidencias de la colaboración conjunta del equipo durante el desarrollo del Sprint 1

## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.
### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.

## 5.4. Video About-the-Product.
