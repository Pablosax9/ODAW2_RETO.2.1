
# Reto 2.1
Nombre y Apellidos: Pablo Rodríguez Crespo
URL del repositorio de gitlab:
**Objetivo:** Aprender a utilizar las propiedades `overflow` y `box-sizing` para manejar el tamaño y el contenido desbordante de elementos en CSS.


## Ejercicio Práctico

1. **Instrucciones**:
   - Crea un archivo `index.html` y un archivo `styles.css`.
   - En el archivo `index.html`, define un contenedor `<div>` con la clase `caja`. Con el siguiente texto`<p>Este es un texto largo que debería desbordar el contenedor para que puedas ver cómo funcionan las propiedades de overflow y box-sizing. Ajusta los estilos en el archivo CSS para ver los cambios.</p>`
   - En el archivo `styles.css`, define estilos para que el contenedor tenga un tamaño fijo, un padding, un border de 2px y un background-color y experimenta con las propiedades `overflow` y `box-sizing`.

2. **HTML** (`index.html`):
   ```html
   <!DOCTYPE html>
   <html lang="es">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Ejercicio CSS - Overflow y Box-sizing</title>
       <link rel="stylesheet" href="styles.css">
   </head>
   <body>
       <div class="caja">
           <p>Este es un texto largo que debería desbordar el contenedor para que puedas ver cómo funcionan las propiedades de overflow y box-sizing. Ajusta los estilos en el archivo CSS para ver los cambios.</p>
       </div>
   </body>
   </html>
   ```

3. **Preguntas**:  
  3.1 Modifica la propiedad `overflow` de la clase `.caja` para ver cómo cambia el comportamiento del contenido desbordante. Adjunta captura.

- Prueba 1: overflow: hidden

  ![alt text](<Captura de pantalla 2024-10-29 212849.png>)

    El contenido que excede el tamaño del contenedor no es visible.

- Prueba 2: overflow: scroll

    ![alt text](<Captura de pantalla 2024-10-29 212949.png>)
    
    Se muestran barras de desplazamiento en ambos ejes, permitiendo desplazarse por el contenido que excede.

- Prueba 3: overflow: auto

    ![alt text](<Captura de pantalla 2024-10-29 213118.png>)

    ![alt text](<Captura de pantalla 2024-10-29 213209.png>)

    Se muestran las barras de desplazamiento solo si el contenido es mayor que el contenedor.

  3.2 Cambia el valor de `box-sizing` a `content-box` y observa cómo el tamaño total del contenedor cambia. Adjunta captura.

  ![alt text](<Captura de pantalla 2024-10-29 214948.png>)

    Si el texto desborda, las barras de desplazamiento aparecen.

    ![alt text](<Captura de pantalla 2024-10-29 215109.png>)

  3.3 Describe qué ocurre con el contenido y el tamaño del contenedor cuando utilizas `overflow: hidden`, `overflow: scroll`, y `box-sizing: border-box`.

  - `overflow: hidden:` El contenido desbordante se oculta. El tamaño del contenedor se mantiene fijo y no se permite el desplazamiento.

  - `overflow: scroll:` Se muestran barras de desplazamiento incluso si el contenido no desborda, permitiendo al usuario desplazarse a través del contenido.

  - `box-sizing: border-box:` Las barras de desplazamiento aparecen solo si el contenido excede el tamaño del contenedor. El tamaño del contenedor permanece constante, pero el comportamiento de visualización del contenido cambia. 

  3.4 ¿Por qué es útil la propiedad `box-sizing` al diseñar interfaces con tamaños fijos?

  La propiedad `box-sizing` es útil porque hace que el tamaño de un elemento (ancho y alto) incluya el padding y el borde. Esto significa que cuando estableces un tamaño fijo, no tienes que preocuparte por calcular cuánto espacio adicional ocupan el padding y el borde, lo que facilita mantener un diseño limpio y predecible.

  3.5 ¿En qué situaciones sería adecuado usar `overflow: auto`?

    Usar `overflow: auto` es adecuado cuando no estás seguro del contenido que tendrá un contenedor. Permite que aparezcan barras de desplazamiento solo si el contenido se desborda. Esto es útil para listas largas, cajas de texto en formularios o secciones de contenido dinámico, asegurando que el diseño se mantenga ordenado sin desbordes visuales.