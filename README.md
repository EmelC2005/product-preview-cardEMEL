# 🛍️ Product Preview Card Component

Este proyecto es una solución al reto [Product preview card component](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa) de Frontend Mentor. Consiste en crear una tarjeta de producto con diseño responsive usando HTML y CSS.

## 🧱 Estructura del Proyecto

```
├── index.html          # Maquetación principal en HTML
├── style.css           # Estilos del componente
└── images/
    ├── image-product-desktop.jpg
    ├── image-product-mobile.jpg
    └── icon-cart.svg
```

## 🎨 Diseño y Estética

### 📐 Diseño Desktop

- Tarjeta dividida en dos mitades: imagen (izquierda) y contenido (derecha).
- Dimensiones máximas: `max-width: 600px` para el contenedor `.card`.
- Imagen de escritorio (`image-product-desktop.jpg`) ocupa el 50% del ancho.
- Fuente serif elegante y moderna para el título.
- Espaciado amplio para contenido legible.

### 📱 Diseño Mobile

- Layout en columna (`flex-direction: column`).
- La imagen pasa a ocupar el 100% del ancho y se posiciona arriba del contenido.
- Se aplica un media query para dispositivos con `max-width: 768px`.

## 🎨 Colores utilizados (por nombre y valor HSL)

| Elemento                        | Color                                     |
|---------------------------------|-------------------------------------------|
| Fondo general                   | `hsl(30, 38%, 92%)` (Beige claro)         |
| Fondo tarjeta (`white`)        | `#ffffff`                                 |
| Título principal                | `hsl(212, 21%, 14%)` (Azul oscuro)        |
| Texto descriptivo y secundario | `hsl(228, 12%, 48%)` (Gris)               |
| Precio con descuento           | `hsl(158, 36%, 37%)` (Verde oscuro suave) |
| Precio anterior                | `hsl(228, 12%, 48%)` (Gris claro)         |
| Botón (hover)                  | `hsl(158, 42%, 18%)` (Verde más oscuro)   |

## ✍️ Tipografías

Se usaron dos fuentes de Google Fonts:

- **Montserrat** (`500`, `700`) para los textos secundarios y botones.
- **Fraunces** (`700`) para el título y precio con descuento.

```html
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&display=swap" rel="stylesheet">
```

## 🧑‍💻 HTML Semántico

- Uso de etiquetas semánticas: `<main>`, `<section>`, `<h1>`, `<h2>`, `<p>`.
- Imagen responsive mediante `<picture>` y `<source>` para cambio de imagen entre móvil y escritorio.

```html
<picture>
  <source media="(max-width: 768px)" srcset="images/image-product-mobile.jpg" />
  <img src="images/image-product-desktop.jpg" alt="Gabrielle Essence Eau De Parfum" />
</picture>
```

## 💅 CSS Detallado

### 📦 Estilos base

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### 🧍 Cuerpo

```css
body {
  font-family: 'Montserrat', sans-serif;
  background-color: hsl(30, 38%, 92%);
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
```

### 📄 Contenedor `.card`

```css
.card {
  display: flex;
  max-width: 600px;
  background-color: white;
  border-radius: 0.75rem;
  overflow: hidden;
}
```

### 🖼️ Imagen

```css
.card picture {
  width: 50%;
}

.card picture img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

### 📚 Contenido `.card-content`

```css
.card-content {
  width: 50%;
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
```

### 🧾 Tipografía

```css
.category {
  font-size: 0.75rem;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: hsl(228, 12%, 48%);
}

.title {
  font-family: 'Fraunces', serif;
  font-size: 2rem;
  color: hsl(212, 21%, 14%);
  margin: 1rem 0;
}

.description {
  font-size: 0.875rem;
  color: hsl(228, 12%, 48%);
  line-height: 1.5;
  margin-bottom: 1.5rem;
}
```

### 💰 Precios

```css
.price {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.current-price {
  color: hsl(158, 36%, 37%);
  font-family: 'Fraunces', serif;
  font-size: 2rem;
}

.original-price {
  text-decoration: line-through;
  color: hsl(228, 12%, 48%);
}
```

### 🛒 Botón

```css
.add-to-cart {
  background-color: hsl(158, 36%, 37%);
  color: white;
  border: none;
  padding: 1rem;
  font-weight: 700;
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.add-to-cart:hover {
  background-color: hsl(158, 42%, 18%);
}
```

## 📱 Responsive con Media Queries

```css
@media (max-width: 768px) {
  .card {
    flex-direction: column;
    max-width: 90%;
  }

  .card picture,
  .card-content {
    width: 100%;
  }

  .card picture img {
    width: 100%;
    height: auto;
  }

  .card-content {
    padding: 1.5rem;
  }
}
```

## ✅ Mejoras Finales

- ✔️ Separamos estructura (`HTML`) y presentación (`CSS`).
- ✔️ Diseño completamente responsive.
- ✔️ Imágenes adaptativas usando `<picture>`.
- ✔️ Tipografía elegante y moderna.
- ✔️ Buen contraste y jerarquía visual.

## 📷 Vista previa

- **Desktop**:  
  ![Preview Desktop](images/image-product-desktop.jpg)

- **Mobile**:  
  ![Preview Mobile](images/image-product-mobile.jpg)

## 🚀 Créditos

Inspirado por el reto de [Frontend Mentor](https://www.frontendmentor.io/) y diseñado con amor por 💻 [Tu Nombre Aquí].
