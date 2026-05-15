# Sesión 04 - 10/04  

### Posición del mouse  
(mouseX, mouseY);  
--> Variables de sistema numérico que determinan la posición del mouse en las coordenadas X e Y.  
[Ejercicio01](https://editor.p5js.org/IsaCarvacho/sketches/OqFDUCw1Q)

## Crear nuestras propias variables  

1. Declarar variable
   --> EJ: let circuloMorado=0; (Arriba del setup(){)
2. Incializar variable
   --> EJ: circuloMorado = circuloMorado+1; (Dentro de function draw(){)
3. Usar la variable
   --> EJ: ellipse(circuloMorado, 200, 50,50); (Dentro de function draw(){)

[Ejercicio02](https://editor.p5js.org/IsaCarvacho/sketches/kqNc--L98)

Para declarar variables podemos usar "let" para variables dinámicas y "const" para variables constantes.  
__Antiguamente se usaba var en vez de let, pueden encontrar algunos tutoriales con var.__  

### Javascript Objects  
Nos servirán para organizar nuestro código de una forma adecuada y ordenada.  
Es la forma de agrupar muchas variables dentro de una variable.  

Es una estructura de datos que te permite agrupar valores relacionados bajo un mismo nombre. En lugar de tener muchas variables sueltas, los objetos funcionan como un "contenedor" que organiza la información mediante pares de clave y valor.  
Luego se accede a la información mediante notación de punto.  

random();  
--> Su trabajo es devolver un número aleatorio dentro de un rango que tú definas.  
(width , height);  
[Ejercicio03](https://editor.p5js.org/IsaCarvacho/sketches/jGv2gNOzo)  
[Ejercicio04](https://editor.p5js.org/IsaCarvacho/sketches/xz4Pp7a-u)  
[Ejercicio05](https://editor.p5js.org/IsaCarvacho/sketches/Iun9hPRg7)  

--> Variables integradas en p5, que corresponden a los valores definidos en el createCanvas.  
(windowWidth, windowHeight);  
--> Variables integradas en p5, que permiten ajustar el tamaño del lienzo al tamaño de la ventana del navegador. Se usan en el createCanvas.  
map();  
--> Esta función nos permite convertir un valor de un rango a otro.  
En términos simples: toma un número que está en una "escala" y lo traduce proporcionalmente a una "escala" nueva.  
Sintaxis --> map(valor, min_original, max_original, min_nuevo, max_nuevo)  
[Ejercicio](https://editor.p5js.org/IsaCarvacho/sketches/Et8MU7taq)
