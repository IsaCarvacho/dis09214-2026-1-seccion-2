# Sesión 10 - 12/06  

## Diseño Responsivo (windowResized)  

__Paso 1__  
Crear canvas con dimensiones dinámicas  
--> function setup(){  
createCanvas(windowWidth, windowHeight)  
}  

__Paso 2__  
Crear un evento windowResized()  
Si el usuario estira o encoge la ventana del navegador, el lienzo se
adaptará al tamaño de la ventana en tiempo real.  
--> function windowResized () {
resizeCanvas(windowWidth, windowHeight);
}

__Paso 3__  
Valores de posición y tamaños se tienen que pensar de manera proporcional a esas variables  
Para eso se usa fracciones y proporciones  
EJ: Centro del lienzo: (width / 2, height / 2)  
EJ: A un cuarto de pantalla en eje x (width * 0.25)  

__Paso 4__  
Incluir un factor de referencia  
--> referencia = min(width, height)  
Se crea una variable global (referencia) y la asignamos para que calcule el mínimo  

__Paso 5__  
Usar translate - Push y Pop (Ideal para proyectos complejos)  
En lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para "mover el origen del mundo”.

### Proporciones  
| Porporción | Valor |  
| :--- | ---: |  
| 5% | 0.05 |  
| 25% | 0.25 |  
| 50% | windowWidth / 2, windowHeight / 2, 0.5 |  
| 75% | 0.75 |  
| Centro del lienzo | width / 2 , height / 2 |  

### Distorsión de imagen  
--> loadPixels()  
Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la memoria de acceso rápido (RAM). Se comunica directamente con la tarjeta gráfica píxel por píxel en tiempo real.  
loadPixels() crea un "puente" temporal para que puedas analizar la
información de forma masiva y fluida.  

get(x, y) — Lectura (El "Ojo")
• Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.
• Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales
esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).
• Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una
copia de respaldo completa del lienzo.
set(x, y, nuevoColor) — Escritura (El "Pincel")
• Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por
completo el color que existía ahí.
• Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo
aspecto de la imagen.
updatePixels() — La Actualización
• Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la
pantalla.
• ¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios
en un borrador secreto. updatePixels() es el comando que efectivamente "publica" y
renderiza el resultado final en el lienzo para que el usuario pueda verlo.
