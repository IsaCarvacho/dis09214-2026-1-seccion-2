# Sesión 07 - 15/05  

´´´JavaScript
´´´

## LOOPS  

Loops: Bucle infinito. Serie de instrucciones que se repite indefinidamente mientras no se cumpla una condición previamente establecida.  
--> Estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.  

## WHILE  
Bucles While son utiles para repetir instrucciones mientras una condición sea verdadera. Son como sentencias if que se repite.   
--> while (condición booleana) {si es true ejecuta este código en BUCLE}  
    EJ: mientras (x sea menor o igual que el alto de mi lienzo) {x incrementará 1 cada vez}  
    [Ejercicio01](https://editor.p5js.org/IsaCarvacho/sketches/Ujz_bQc9I)  
    [Ejercicio02](https://editor.p5js.org/IsaCarvacho/sketches/9qJDOVkJr)  
    [Ejercicio03](https://editor.p5js.org/IsaCarvacho/sketches/mQdh-vU4b) No me funcionó jaja :')  

### For 4 ELEMENTOS  
--> for (inicialización variable; condición booleana; actualización)  
{lo que queremos que pase cuando la condición sea verdadera  
}  
    EJ: for(let x=0; x <= width; x=x+1){  
    ellipse (x, 200, random(300))  
    }  
    [Ejercicio04](https://editor.p5js.org/IsaCarvacho/sketches/U8cKzRa49)  
    [Ejercicio05](https://editor.p5js.org/IsaCarvacho/sketches/GBymdOXRE)  

## Nested Loops  
Un loop dentro de otro loop; Un for dentro de otro for  
for (inicialización variable; condición booleana; actualización){  
lo que queremos __!!!__  
* Loop que va primero es el que va adentro

   [Ejercicio06](https://editor.p5js.org/IsaCarvacho/sketches/KZ6wGkjbb)
  [Ejercicio07](https://editor.p5js.org/IsaCarvacho/sketches/2Nor2BKmb)
  [Ejercicio08](https://editor.p5js.org/IsaCarvacho/sketches/NCtMdJsjL)
