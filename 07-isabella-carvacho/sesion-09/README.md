# Sesión 09 - 29/05  

## Diagramas de flujo  
### Algoritmo  
--> Secuencia de instrucciones paso a paso, lógicas, definidas, ordenadas y finitas que permiten solucionar un problema o realizar una tarea específica.  
- Precisión: Cada paso debe estar clarísimo (sin ambigüedades)
- Orden: Los pasos llevan una secuencia lógica.
- Finitud: Tiene que terminar en algún momento; no puede ser finito.
- Definición: Si sigues el mismo algoritmo dos veces con los mismos datos, deberías obtener siempre el mismo resultado.

#### Estructura  
--> Input (Entrada), Proceso, Output (Salida)  

## Arrays (listas)  
Array: Un contenedor con compartimentos numerados donde puedes guardar múltiples datos bajo un mismo nombre. Es una lista que mantiene varios datos ordenados. Los arreglos (Arrays) son muy útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.  
--> Como por ejemplo: Tren con vagones (un tren de programación, por así decirlo): el tren en sí es el array, pero cada vagón es un elemento, y cada elemento puede contener lo que quieras.  
__Sintaxis:__ let nombreArray =[e0, e1, e2, e3, e4, e5];  
--> let Colores = ["red", "orange", "yellow", "green", "blue"];  
¿Cómo se usan los elementos del Array?  
--> Para llamar a alguno de los valores de mi array vamos a usar: nombreArray [n° elemento ]  
EJ: background (colores[1]); //Esto pintará el fondo de mi lienzo de color anaranjado.  
[Ejercicio01](https://editor.p5js.org/IsaCarvacho/sketches/8igAzqKAF) 
[Ejercicio2](https://editor.p5js.org/IsaCarvacho/sketches/4jMWIhRof)  
[Ejercicio3](https://editor.p5js.org/IsaCarvacho/sketches/X6B96uT4g)  
[Ejercicio4](https://editor.p5js.org/IsaCarvacho/sketches/if0svhX9R)  
[Ejercicio5](https://editor.p5js.org/IsaCarvacho/sketches/q2u-2BM2V)  

## Class (molde)  
Class: Una clase (class) es un molde o plantilla abstracta que define la estructura, los datos (propiedades) y los comportamientos (métodos) que tendrá un tipo de objeto específico.  
--> Como por ejemplo: Plano de diseño de una casa o un cortador de galletas: no es el objeto real en sí, sino las instrucciones empaquetadas para fabricar infinitas
copias independientes basadas en ese mismo modelo utilizando la palabra clave new.  
__Sintaxis:__ La sintaxis básica de una clase en JavaScript se estructura siempre en tres partes dentro de un bloque de llaves:  
1. La palabra clave class + nombre que le quiera dar.
2. El método constructor (donde se definen las propiedades del objeto usando .this)
3. Las funciones personalizadas que definen lo que hace el objeto.

--> class se escribe afuera y abajo de la función draw();  
    Luego se crea en el setup();  
    Y se llama a sus métodos en el draw();  
[Ejercicio6](https://editor.p5js.org/IsaCarvacho/sketches/35guUxbiT)  

## Class + Array  
[Ejercicio7](https://editor.p5js.org/IsaCarvacho/sketches/gN_kHh_I0)  
[Ejercicio8](https://editor.p5js.org/IsaCarvacho/sketches/Rd8SH_g-Y)  
[Ejercicio9](https://editor.p5js.org/IsaCarvacho/sketches/lhPjwcTe4)  
[Ejercicio10](https://editor.p5js.org/IsaCarvacho/sketches/VnHmzxprp) 
