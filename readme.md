### ink-web

**Modelo de publicación web pensado para dispositivos de tinta electrónica**

Este proyecto es un ejemplo funcional del modelo **ink-web**:
una forma de diseñar y publicar sitios web y revistas digitales pensadas primero para pantallas e-ink (Kindle y dispositivos similares).

Ink-web prioriza:

* lectura profunda
* navegación simple
* compatibilidad con navegadores limitados
* contenido que puede existir como web **y** como revista (EPUB / AZW3)

---

## Estructura del sitio (jerarquía ink-web)

El sitio está compuesto por **HTML estático**, organizado en tres niveles claros:

### 1° nivel — Inicio

**`index.html`**

Es la portada del sitio.
Desde aquí se accede a las categorías (segundo nivel).

Puede editarse con cualquier editor de texto simple
(Bloc de notas, Xed, Nano, etc.).

---

### 2° nivel — Categorías

Archivos como:

* `columnas.html`
* `viajes.html`
* `resenas.html`
* `academia.html`
* `artes.html`
* `clasicos.html`
* `acerca.html`

Cada archivo representa una **categoría**.

Características:

* nombre de la categoría
* ícono de “casa” para volver a `index.html`
* autores y artículos separados en dos columnas
* navegación simple y predecible

---

### 3° nivel — Artículos

Cada archivo corresponde a un artículo individual.

Elementos comunes:

* barra superior con:

  * título del artículo
  * ícono de casa (volver al inicio)
  * ícono de menú (volver a la categoría)
* botones laterales para pasar página
* numeración de página en la esquina superior derecha

Este nivel está pensado para **lectura prolongada en e-ink**.

---

## Plantillas para clonar el sitio

Clonar y crear una versión propia es intencionalmente sencillo.

Archivos de plantilla:

* **`plantillaindex.html`**
  → úsala para crear tu propio `index.html`

* **`plantillacategoria.html`**
  → úsala para crear tus categorías (segundo nivel)

* **`plantillarticulo.html`**
  → úsala para crear artículos (tercer nivel)

En cada plantilla:

* reemplaza todo lo que diga **“inserta aquí”**
* cambia nombres, enlaces y textos según tu contenido

No se requiere ningún framework ni herramienta adicional.

---

## Probar el sitio en un Kindle u otro dispositivo e-ink

### En tu ordenador

Usa dos terminales.

**Terminal 1**
Dentro de la carpeta del sitio:

```
python3 -m http.server 8000
```

Esto levanta un servidor local.

**Terminal 2**

```
hostname -I
```

Obtendrás tu dirección IP local.

---

### En el Kindle

1. Abre el navegador
2. Escribe:

```
http://TU_IP:8000
```

3. Se cargará el sitio ink-web desde tu ordenador

---

## Publicación como revista

Este proyecto también se compila periódicamente como:

* EPUB
* AZW3

De este modo, el mismo contenido puede leerse:

* como sitio web
* como revista digital descargable

Este puente entre **web y libro** es parte central del modelo ink-web.

---

## Licencia y uso

Este proyecto puede ser bifurcado, adaptado y reutilizado libremente.
Si haces tu propia edición, estás expandiendo ink-web.
-------
