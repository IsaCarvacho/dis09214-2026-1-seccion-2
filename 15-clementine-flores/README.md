

# "Supremacía de minorías"
## Katalina Ludueña y Clementine Flores

### Descripción objetiva
#### ¿Qué es el proyecto?
Nuestro proyecto representa en cómo en la actualidad y durante siglos, la supremacía del hombre (cis-hetero-opresores) ante las personas no hombres (mujeres, lesbianas, trans, no binares, etc).

#### ¿Qué se ve en pantalla?
Se ve la opresión, la incomodidad y la inseguridad que han causado y siguen causando los hombres cis-hetero/opresores a toda persona no hombre, y también se muestra un mundo ideal en el que no existe esta opresión y florece la libertad como un lugar seguro en donde puedes ser tu mismx. 
¿Qué elementos visuales aparecen?
*  Figuras geométricas representadas como las personas no hombres (mujeres, lesbianas, trans, no binaries, etc)
*  Símbolo de hombre (supremacía cis-hetero)
*  Frase dicha por Violeta Parra "Soy una hormiguita que busca bajo la tierra dónde poder refugiar su corazón", asociando "hormigas" como esta minoría no hombre.
*  Una imagen de un símbolo masculino y otra imagen de un lirio florecido.

#### Descripción conceptual
Nuestra idea central del proyecto y la relación con nuestro sistema diseñado, es demostrar la realidad actual y no actual, de cómo las personas no hombres son oprimidas. Nuestra regla de oro en el proyecto funciona de esta manera: Mientras el mouse esté presionado, persiste la supremacía y opresión, pero al soltarlo, las personas no hombres pueden florecer libremente en este mundo ideal, o conviviendo con las mismas personas no hombres. La lógica con nuestra problemática se relaciona directamente en representación desde nosotras, como personas no hombres oprimidas por la supremacía diariamente, en cómo nosotras lo hemos vivido, y en que sabemos cómo puede ser vivenciarlo desde primera fuente. 

#### Input / Output y sistema
¿Qué datos entran? (INPUT)
*  La posición del mouse (mouseX y mouseY), que determina dónde aparece el símbolo masculino.
*  La acción de presionar o soltar el mouse (mousePressed() y mouseReleased()), que cambia el estado de la variable opresion.
*  Las imágenes cargadas al inicio (simbolo masculino.png y fondo.jpeg).
*  Los valores aleatorios generados para cada figura, como su posición inicial, tamaño, velocidad, tipo y color.

#### Cómo se procesan y transforman?
Las figuras se desplazan según sus velocidades horizontal y vertical, cuando llegan a los bordes del lienzo, rebotan cambiando la dirección de su movimiento, se calcula la distancia entre cada figura y el símbolo masculino, si una figura se encuentra a menos de 200 píxeles del símbolo, se aleja de él y además presenta un pequeño temblor aleatorio, cuando se presiona el mouse, la variable opresion cambia a true, desaparece el símbolo masculino y se muestra una imagen de fondo. Cuando se suelta el mouse, opresion vuelve a false, reaparece el símbolo masculino y las figuras vuelven a reaccionar ante él. El color de las figuras también cambia según el estado de opresión: son grises cuando el símbolo masculino está presente y recuperan sus colores cuando desaparece.

#### Qué respuesta visual producen? (OUTPUT)
*  Las figuras se desplazan según sus velocidades horizontal y vertical. 
*  Cuando llegan a los bordes del lienzo, rebotan cambiando la dirección de su movimiento.
*  Se calcula la distancia entre cada figura y el símbolo masculino.
*  Si una figura se encuentra a menos de 200 píxeles del símbolo, se aleja de él y además presenta un pequeño temblor aleatorio.
*  Cuando se presiona el mouse, la variable opresion cambia a true, desaparece el símbolo masculino y se muestra una imagen de fondo.
*  Cuando se suelta el mouse, opresion vuelve a false, reaparece el símbolo masculino y las figuras vuelven a reaccionar ante él.
*  l color de las figuras también cambia según el estado de opresión: son grises cuando el símbolo masculino está presente y recuperan sus colores cuando desaparece.

#### Pensamiento computacional
Reglas que gobiernan el sistema (inputs, procesos, outputs)
#### Explicación del sistema de interactividad
La interactividad de este proyecto se basa en el uso del mouse como elemento de control. El usuario puede mover el cursor por la pantalla, haciendo que el símbolo masculino siga su posición. Este símbolo funciona como un agente de opresión, ya que las figuras que representan lo no hombre reaccionan a su cercanía alejándose de él.

El sistema responde a la acción de presionar y soltar el mouse. Cuando el usuario presiona el botón del mouse, la variable opresion cambia de estado, provocando que el símbolo masculino desaparezca, que el fondo se transforme en una imagen de una flor que florece y que las figuras recuperen sus colores vibrantes. Al soltar el mouse, el estado vuelve a la normalidad: reaparece el símbolo masculino, el fondo vuelve a ser gris y las figuras se muestran nuevamente en tonos grises mientras continúan reaccionando a la presencia del símbolo.

De esta manera, la interacción permite que el usuario altere directamente el comportamiento visual de la composición, generando un contraste entre dos estados: uno asociado a la opresión y otro asociado a la liberación. El movimiento del cursor y el clic del mouse son los mecanismos que activan estos cambios y construyen el significado de la obra.

#### Referentes
Listado y breve descripción de referentes visuales, teóricos o históricos.
• Diagrama de Flujo (Imagen en PNG ) (Agregada en formato MarkDown)
• Código de p5.js (Agregado en formato MarkDown)
• Link al sketch en P5.js en formato EDITABLE.
