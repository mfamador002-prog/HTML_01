# 🧱 Fundamentos de HTML

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Nivel](https://img.shields.io/badge/Nivel-Principiante-brightgreen?style=for-the-badge)
![Licencia](https://img.shields.io/badge/Licencia-MIT-blue?style=for-the-badge)

Guía práctica para aprender las bases de **HTML** (HyperText Markup Language), el lenguaje que define la estructura de cualquier página web. Incluye explicaciones cortas, ejemplos listos para copiar y ejercicios para practicar.

---

## 📑 Tabla de contenido

1. [¿Qué es HTML?](#-qué-es-html)
2. [Requisitos](#-requisitos)
3. [Estructura del repositorio](#-estructura-del-repositorio)
4. [Estructura básica de un documento](#-estructura-básica-de-un-documento)
5. [Etiquetas y atributos](#-etiquetas-y-atributos)
6. [Texto y encabezados](#-texto-y-encabezados)
7. [Listas](#-listas)
8. [Enlaces e imágenes](#-enlaces-e-imágenes)
9. [Tablas](#-tablas)
10. [Formularios](#-formularios)
11. [HTML semántico](#-html-semántico)
12. [Accesibilidad](#-accesibilidad)
13. [Buenas prácticas](#-buenas-prácticas)
14. [Ejercicios](#-ejercicios)
15. [Recursos](#-recursos)
16. [Contribuir](#-contribuir)
17. [Licencia](#-licencia)

---

## 🌐 ¿Qué es HTML?

HTML es un **lenguaje de marcado**, no de programación. Sirve para decirle al navegador *qué es* cada parte del contenido: un título, un párrafo, una imagen, un enlace, etc.

| Tecnología | Rol |
|---|---|
| **HTML** | Estructura (el esqueleto) |
| **CSS** | Presentación (el estilo) |
| **JavaScript** | Comportamiento (la interacción) |

---

## 🛠 Requisitos

- Un editor de código (recomendado: [Visual Studio Code](https://code.visualstudio.com/))
- Un navegador moderno (Chrome, Firefox, Edge, Safari)
- Opcional: extensión **Live Server** en VS Code para ver cambios en tiempo real

### Cómo usar este repo

```bash
# Clona el repositorio
git clone https://github.com/tu-usuario/fundamentos-html.git

# Entra a la carpeta
cd fundamentos-html
```

Abre cualquier archivo `.html` con doble clic o con Live Server.

---

## 📂 Estructura del repositorio

```
fundamentos-html/
├── 01-estructura-basica/
│   └── index.html
├── 02-texto/
├── 03-listas/
├── 04-enlaces-imagenes/
├── 05-tablas/
├── 06-formularios/
├── 07-semantica/
├── ejercicios/
└── README.md
```

---

## 🦴 Estructura básica de un documento

Todo archivo HTML parte de este esqueleto:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi primera página</title>
</head>
<body>
  <h1>¡Hola, mundo!</h1>
  <p>Esta es mi primera página web.</p>
</body>
</html>
```

| Elemento | ¿Para qué sirve? |
|---|---|
| `<!DOCTYPE html>` | Indica que el documento usa HTML5 |
| `<html lang="es">` | Elemento raíz; `lang` define el idioma |
| `<head>` | Información que no se ve (metadatos, título, estilos) |
| `<meta charset="UTF-8">` | Permite acentos, ñ y caracteres especiales |
| `<meta name="viewport">` | Hace que la página se adapte a celulares |
| `<title>` | Texto que aparece en la pestaña del navegador |
| `<body>` | Todo el contenido visible |

---

## 🏷 Etiquetas y atributos

Una **etiqueta** abre y cierra un elemento. Los **atributos** agregan información extra.

```html
<a href="https://github.com" target="_blank">Ir a GitHub</a>
<!-- │   └── atributo ──┘  └── atributo ──┘                │ -->
<!-- └── etiqueta de apertura          etiqueta de cierre ─┘ -->
```

Algunas etiquetas **no se cierran** (elementos vacíos):

```html
<br>   <!-- salto de línea -->
<hr>   <!-- línea horizontal -->
<img src="foto.jpg" alt="Descripción">
<input type="text">
```

Atributos globales más usados: `id`, `class`, `style`, `title`, `lang`, `hidden`.

---

## ✍ Texto y encabezados

```html
<h1>Título principal</h1>
<h2>Subtítulo</h2>
<h3>Sección</h3>
<!-- ... hasta <h6> -->

<p>Un párrafo normal.</p>
<p>Texto <strong>importante</strong> y texto <em>enfatizado</em>.</p>
<p>Fórmula del agua: H<sub>2</sub>O. Área: m<sup>2</sup>.</p>
<blockquote>Una cita larga.</blockquote>
<code>console.log("código en línea")</code>
```

> 💡 Usa **un solo `<h1>`** por página y respeta el orden jerárquico (no brinques de `h2` a `h5`).

---

## 📋 Listas

```html
<!-- Lista desordenada -->
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>

<!-- Lista ordenada -->
<ol>
  <li>Crear el archivo</li>
  <li>Escribir la estructura</li>
  <li>Abrir en el navegador</li>
</ol>

<!-- Lista de definiciones -->
<dl>
  <dt>HTML</dt>
  <dd>Lenguaje de marcado para estructurar contenido.</dd>
</dl>
```

---

## 🔗 Enlaces e imágenes

```html
<!-- Enlace externo (abre en otra pestaña) -->
<a href="https://developer.mozilla.org" target="_blank" rel="noopener">MDN</a>

<!-- Enlace a otra página del sitio -->
<a href="contacto.html">Contacto</a>

<!-- Enlace a una sección de la misma página -->
<a href="#formularios">Ir a formularios</a>

<!-- Enlace de correo y teléfono -->
<a href="mailto:hola@ejemplo.com">Escríbenos</a>
<a href="tel:+524491234567">Llámanos</a>

<!-- Imagen -->
<img src="img/logo.png" alt="Logo de la empresa" width="200">

<!-- Imagen con pie de foto -->
<figure>
  <img src="img/paisaje.jpg" alt="Montañas al atardecer">
  <figcaption>Atardecer en la sierra.</figcaption>
</figure>
```

> ⚠️ El atributo `alt` **siempre** debe describir la imagen. Es clave para accesibilidad y SEO.

---

## 📊 Tablas

```html
<table>
  <caption>Precios de productos</caption>
  <thead>
    <tr>
      <th>Producto</th>
      <th>Precio</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Playera</td>
      <td>$250</td>
    </tr>
    <tr>
      <td>Gorra</td>
      <td>$180</td>
    </tr>
  </tbody>
</table>
```

| Etiqueta | Significado |
|---|---|
| `<table>` | Contenedor de la tabla |
| `<tr>` | Fila (*table row*) |
| `<th>` | Celda de encabezado |
| `<td>` | Celda de datos |
| `<thead>` / `<tbody>` / `<tfoot>` | Agrupan encabezado, cuerpo y pie |

> 💡 Usa tablas solo para **datos tabulares**, nunca para acomodar el diseño de la página.

---

## 📝 Formularios

```html
<form action="/enviar" method="POST">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>

  <label for="correo">Correo:</label>
  <input type="email" id="correo" name="correo" required>

  <label for="edad">Edad:</label>
  <input type="number" id="edad" name="edad" min="1" max="120">

  <label for="plan">Plan:</label>
  <select id="plan" name="plan">
    <option value="basico">Básico</option>
    <option value="pro">Pro</option>
  </select>

  <p>¿Cómo nos conociste?</p>
  <input type="radio" id="redes" name="origen" value="redes">
  <label for="redes">Redes sociales</label>
  <input type="radio" id="amigo" name="origen" value="amigo">
  <label for="amigo">Un amigo</label>

  <input type="checkbox" id="terminos" name="terminos" required>
  <label for="terminos">Acepto los términos</label>

  <label for="mensaje">Mensaje:</label>
  <textarea id="mensaje" name="mensaje" rows="4"></textarea>

  <button type="submit">Enviar</button>
</form>
```

Tipos de `input` más comunes: `text`, `email`, `password`, `number`, `tel`, `date`, `checkbox`, `radio`, `file`, `range`, `color`.

---

## 🧭 HTML semántico

Las etiquetas semánticas describen **el significado** del contenido, no solo su apariencia.

```html
<body>
  <header>
    <nav>
      <a href="#">Inicio</a>
      <a href="#">Servicios</a>
    </nav>
  </header>

  <main>
    <article>
      <h1>Título del artículo</h1>
      <section>
        <h2>Primera sección</h2>
        <p>Contenido...</p>
      </section>
    </article>

    <aside>Contenido relacionado</aside>
  </main>

  <footer>
    <p>&copy; 2026 Mi sitio</p>
  </footer>
</body>
```

| Etiqueta | Uso |
|---|---|
| `<header>` | Encabezado de la página o sección |
| `<nav>` | Menú de navegación |
| `<main>` | Contenido principal (uno por página) |
| `<article>` | Contenido independiente (post, noticia) |
| `<section>` | Agrupación temática con título |
| `<aside>` | Contenido secundario o lateral |
| `<footer>` | Pie de página o sección |

**`<div>` vs semántica:** usa `<div>` y `<span>` solo cuando ninguna etiqueta semántica encaje.

---

## ♿ Accesibilidad

- Escribe `alt` descriptivos en todas las imágenes.
- Asocia cada `<label>` con su `<input>` usando `for` e `id`.
- Respeta la jerarquía de encabezados.
- Declara el idioma con `<html lang="es">`.
- Usa `<button>` para acciones y `<a>` para navegación.
- Cuida el contraste de colores (esto ya es con CSS, pero tenlo en mente).

---

## ✅ Buenas prácticas

- Escribe etiquetas y atributos en **minúsculas**.
- **Indenta** el código para que sea fácil de leer.
- Cierra siempre las etiquetas que lo requieren.
- Usa comillas dobles en los atributos: `class="menu"`.
- Nombra archivos sin espacios ni acentos: `mi-pagina.html`.
- Separa la estructura (HTML) del estilo (CSS) y la lógica (JS).
- Valida tu código con el [W3C Validator](https://validator.w3.org/).
- Comenta secciones importantes:

```html
<!-- ===== Sección de contacto ===== -->
```

---

## 🏋 Ejercicios

- [ ] **Ejercicio 1:** Crea una página con tu nombre como `<h1>` y un párrafo sobre ti.
- [ ] **Ejercicio 2:** Agrega una lista con tus 5 películas favoritas.
- [ ] **Ejercicio 3:** Inserta una imagen con su `alt` y un enlace a tu red social.
- [ ] **Ejercicio 4:** Haz una tabla con tu horario de la semana.
- [ ] **Ejercicio 5:** Construye un formulario de contacto con nombre, correo y mensaje.
- [ ] **Reto final:** Arma una página de portafolio usando solo etiquetas semánticas.

---

## 📚 Recursos

- [MDN Web Docs – HTML](https://developer.mozilla.org/es/docs/Web/HTML)
- [W3Schools – HTML](https://www.w3schools.com/html/)
- [HTML Living Standard (WHATWG)](https://html.spec.whatwg.org/)
- [W3C Markup Validator](https://validator.w3.org/)
- [Can I use](https://caniuse.com/) – compatibilidad entre navegadores

---

## 🤝 Contribuir

1. Haz un **fork** del proyecto.
2. Crea una rama: `git checkout -b mejora/nueva-seccion`
3. Haz commit de tus cambios: `git commit -m "Agrega sección de multimedia"`
4. Sube la rama: `git push origin mejora/nueva-seccion`
5. Abre un **Pull Request**.

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Consulta el archivo [`LICENSE`](LICENSE) para más detalles.

---

<p align="center">Hecho con ❤️ y mucho <code>&lt;html&gt;</code></p>
