# Sesión 09 - 05/06  

## Estados y cámara web  

__Paso 1__  
Crear y definir variable estados  
Al principio de tu código (fuera de las funciones), debes crear una variable que guarde en qué pantalla nos encontramos. Empezará en 0.  
--> let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final  

__Paso 2__  
Configurar el lienzo (function setup)  
Creamos el lienzo de fondo.  
--> function setup() {  
createCanvas(400,400);  
textAlign(CENTER, CENTER);  
textSize(24);  
}  

__Paso 3__  
Crear la estructura del estado (function draw)  
Aquí usamos un switch. Dependiendo del valor de la variable estado, el programa
dibujará una cosa u otra.  

__Paso 4__   
Programar visualmente cada estado (funciones propias)  
Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.  

__Paso 5__  
La lógica del cambio y el reinicio  
Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función
mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.  

### Formas de cambiar de un estado a otro  
1. Interacción con el teclado
   1.1. Por barra espaciadora o Enter
   1.2. Por teclas específicas (ej. Números): Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.
2. Botones reales en pantalla
   2. En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando la librería de p5.js. Esto es mucho más profesional para menús.
3. Zonas de click (Botones dibujados con rect o ellipse)
  3. Si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(), puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.
4. Interacciones automáticas (Por tiempo)
   4. Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que dura 3 segundos y pasa sola al menú.
  
## Cámara web  
--> createCapture(VIDEO);  
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.
2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del
computador. También definimos tamaño con captura.size(x,y); y es muy importante
agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.
