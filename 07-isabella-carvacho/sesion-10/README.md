# Sesión 10 - 12/06  

## Diseño Responsivo (windowResized)  

__Paso 1__  
Crear canvas con dimensiones dinámicas  
--> function setup(){  
createCanvas(windowWidth, windowHeight)  
}  

__Paso 2__  
Valores de posición y tamaños se tienen que pensar de manera proporcional a esas variables  
Para eso se usa fracciones y proporciones  
EJ: Centro del lienzo: (width / 2, height / 2)  
EJ: A un cuarto de pantalla en eje x (width * 0.25)  

__Paso 4__  
Incluir un factor de referencia  
--> referencia = min(width, height)  
Se crea una variable global (referencia) y la asignamos para que calcule el mínimo  

### Proporciones  
| Porporción | Valor |  
| :--- | ---: |  
| 50% | windowWidth / 2, windowHeight / 2, 0.5 |  
| 25% | 0.25 |
