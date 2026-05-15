# Sesión 03 - 27/03  

## Algoritmo  
Secuencia de instrucciones paso a paso, lógicas, definidas, ordenadas y finitas que permiten solucionar un problema o realizar una tarea específica.  

### Su estructura  
Su estructura consta de el Input (Entrada), el Proceso y el Output (Salida). El algoritmo recibe instrucciones de que hacer en distintas situaciones.  
Por ejemplo:  
"La lámpara no funciona" --> ¿Esta enchufada la lámpara?  
"No" --> Enchufar la lámpara
"Sí" --> "¿Está quemada la ampolleta?"  
"Sí" --> Camiar la ampolleta  
"No" --> Comprar nueva lámpara  

Existen entre 700 y 900 lenguajes de programación que se utilizan actualmente. Si incluimos lenguajes antiguos, dialectos específicos y lenguajes creados para investigación, la cifra supera los 8.000 o incluso 9.000.  

p5.js por ejemplo utiliza JavaScript principalmente, usa su biblioteca, osea toda la potencia y sintaxis de JavaScript, pero con un "vocabulario" especializado para dibujar, animar y crear elementos visuales de forma mucho más sencilla.  

### Funciones maestras  
__setup (){}__ --> Se ejecuta una sola vez al principio. Configura el entorno inicial. Se define el tamaño del lienzo (createCanvas), cargas imágenes o sonidos y estableces configuraciones que no cambiarán (como el color de fondo incial).  

__draw (){}__ --> Se ejecuta en un bucle infinito (normalmente 60 veces por segundo), lo que permite crear animaciones. Crea movimiento y responde a la interacción en tiempo real. Dibujas formas que cambian de posición, detectas dónde está el ratón o
cambias colores gradualmente.  

### Funciones  
createCanvas ([width], [height], [renderer], [canvas]);  
--> Nos sirve para crear un lienzo y determinar su tamaño en pixeles. __Solo se ejecuta una vez y siempre dentro del setup()__  
background(v1, v2, v3, [a]);  
--> Sirve para designar el color de nuestro lienzo en valores RGB. [a] es el parámetro para el canal alpha, nos sirve para darle semitransparencia al color
del fondo. (0-255) Donde 1 será muy transparente y 255 muy poco transparente. No es necesario usar este parámetro. __Depende si dejamos esta función el setup o el draw el resultado que se obtenga.  

__Se debe tener en cuenta que p5.js trabaja con coordenadas x e y. El punto 0,0 no esta al centro, si no en la esquina superior derecha.__  

### Figuras geométricas.  
• point(x, y); Dibuja un solo píxel en las coordenadas dadas.  
• line(x1, y1, x2, y2); Dibuja una línea desde un punto inicial hasta un punto final.  
• rect(x, y, ancho, alto); Dibuja un rectángulo. Por defecto, x e y definen la esquina superior izquierda.  
• ellipse(x, y, ancho, alto); Dibuja un óvalo o círculo. A diferencia del rectángulo, x e y definen el centro de la figura.  
• circle(x, y, diámetro); Una versión simplificada de la elipse cuando quieres un círculo perfecto.  
• square(x, y, lado); Un rectángulo donde todos los lados son iguales.  
• triangle(x1, y1, x2, y2, x3, y3); Necesitas darle las coordenadas de sus tres esquinas.  
• quad(x1, y1, x2, y2, x3, y3, x4, y4); Un cuadrilátero. Sirve para hacer formas irregulares de cuatro lados.  

strokeWeight(weight);  
--> Establece el tamaño del borde
de las figuras o el ancho de la linea o punto. Siempre se pone arriba de Stroke();  
stroke(v1, v2, v3, [alpha]);  
--> Establece el color que se utiliza para dibujar puntos, lineas y contornos de figuras. Se pone arriba de la linea de código de la figura.
noStroke(); 
--> Se usa para que la figura no tenga borde.  
strokeCap(cap);  
--> Define la forma de la linea o borde de nuestras figuras. Por defecto es ROUND pero también estan SQUARE y PROJECT. 
fill(v1, v2, v3, [alpha]);  
--> Establece el color de relleno para las figuras. Se pone arriba de la figura que quiero colorear.  
arc(x, y, w, h, start, stop);  
--> Nos sirve para hacer arcos o medio círculo. X e y son las coordenadas del centro del círculo que contiene este arco, w y h son la anchura y alto del círculo que contiene este arco, star y stop, es donde comienza y termina el ángulo de este arco. __Para esta función es bueno ejecutar angleMode(DEGREES); en el setup(); para tener un sistema de ángulos más amigable.__  

### Desafíos de la clase  
[Desafío1p5.js](https://editor.p5js.org/IsaCarvacho/sketches/4dHp4GKWlK)  
[Desafío2p5.js](https://editor.p5js.org/IsaCarvacho/sketches/taiXxlXly)
