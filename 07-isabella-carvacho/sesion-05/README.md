# Sesión 05 - 17/04  

## Transformaciones y Condicionales {if - else}

__Radial__: Medida geometria. Perimetro afuera mide lo mismo que el radio que los circusnscribe. Radio coincide con perimetro. (Metodo que no usa el angleMode)  

__angleMode();__  
--> Siempre el cero parte en las "3 de la tarde". 

Por defecto el programa usa __RADIANES__ para medir ángulos. angleMode(RADIANES). Para cambiar a grados se usa esto en el fuction setup();  

__ROTACIÓN__  
rotate();  
--> Los puntos siempre van a rotar en base del punto 0°. Se recomienda empezar con mi figura en el punto 0,0, y luego aplicar rotate o translate.  
[Ejercicio01](https://editor.p5js.org/IsaCarvacho/sketches/8A7eZMi5s)  

__TRANSLATE__  
translate();  
--> Trasladar el punto de origen (0,0) a otra coordenada de el canvas.  
[Ejercicio02](https://editor.p5js.org/IsaCarvacho/sketches/lTHMG58kH)

__GUARDAR Y RESTAURAR__
push();  
pop();  
--> Los códigos de adentro no afectan al resto de los otros códigos. Funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo.  
[Ejercicio03](https://editor.p5js.org/IsaCarvacho/sketches/ecist0L-1)

__ESCALA__ scale(); --> La función scale() ajusta la escala del sistema de coordenadas actual por el factor especificado.  
[Ejercicio04](https://editor.p5js.org/IsaCarvacho/sketches/KU5Ujd8Sx)

## Condicionales
Expresión booleana: Cualquier dato que al evaluarlo arroja dos resultados posibles, true o false. 
Se necesitan los operandos (o valores), operadores de comparación y los operadores lógicos. 
Operandos (o valores) --> Datos básicos que se evaluan. Pueden ser variables como:
- Variables (x, y, o mouseX, mouseY, etc)
- Constantes o literales 

### IF - ELSE IF - ELSE
__if__  
--> Toma una condición -expresada como un booleando- y ejecuta una pieza de código contenida dentro de las llaves { }  
if (condición booleana){ejecuta este código si es true}  
__else if__  
--> Añade condiciones de prueba complementarias a la original  
else if (condición 2) {ejecuta este código si es true}  
__else__  
--> Implica todos los casos que no cumplen con la condicón original  
else {ejecuta este código si ambas condiciones son falsas}  
[Ejercicio05](https://editor.p5js.org/IsaCarvacho/sketches/hzUIOKgbq)  
[Ejercicio06](https://editor.p5js.org/IsaCarvacho/sketches/meOMnHxja)  
[Ejercicio07](https://editor.p5js.org/IsaCarvacho/sketches/Ogm6_SwIP)
