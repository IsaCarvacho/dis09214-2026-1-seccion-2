# Solemne_02  

## Trabajo No Remunerado Del Hogar (TNR)  

[![Banner](https://i.pinimg.com/736x/be/35/02/be3502efceb4e4145057455b95ed5c75.jpg)](https://cl.pinterest.com/pin/585186545373271588/)

En esta solemne me gustaría hablar de el trabajo no remunerado del hogar (TNR) comprende las labores domésticas y de cuidados realizadas sin salario, esenciales para el bienestar familiar y el funcionamiento económico.  

La presidenta del directorio de ComunidadMujer, María Olivia Recart, destacó que el [informe](https://www.hacienda.cl/noticias-y-eventos/noticias/ministerio-de-hacienda-y-comunidadmujer-lanzan-estudio-que-valoriza-el-trabajo) establece que “más de dos tercios del trabajo doméstico y de cuidados no remunerado lo realizan mujeres, que dedican en promedio más de cinco horas diarias a estas tareas. Este estudio visibiliza esa economía subterránea, invisible en las cuentas nacionales pero esencial para que todo lo demás funcione. Reconocerla es el primer paso para construir un país que valore y redistribuya los cuidados”, indicó.  

El estudio establece que el __trabajo doméstico y de cuidados no remunerado equivale al 19,2% del PIB Ampliado de Chile (2023), lo que lo convierte en el mayor sector económico del país; y el aporte de las mujeres a esta actividad económica representa el 65,2% del valor total,__ equivalente al 12,5% del PIB Ampliado.  

#### Me parece súper importante hablar de esto ya que tomando en cuenta la información, es una labor que sostiene a un país entero desde la invisibilidad.  

### Trabajo No Remunerado Del Hogar (TNR); Conceptos asociados  
__Invisibilización:__ La invisibilización es el proceso cultural y sociopolítico mediante el cual grupos de poder hegemónicos omiten, marginan o desvalorizan a ciertos sectores sociales (como mujeres, minorías étnicas o disidencias). Se manifiesta a través del lenguaje, la discriminación y la omisión en las políticas públicas, negando la existencia y aportes de estas comunidades.  
__Dependencia:__ Relación de necesidad constante hacia una sustancia, actividad o vínculo emocional, que se mantiene aunque esté provocando consecuencias negativas.  

### Abstracción de la problemática  
Invisible --> Todo aquello que no puede ser visto o que es imperceptible para la vista. Carece de presencia notoria.   
Transparencia. Tonos grises, blancos y negros. Siluetas difuminadas. 

![inivisible](https://i.pinimg.com/736x/02/14/62/0214629dd5d804c061fa4d1831916e64.jpg)  

Dependencia --> Un elemento (o varios) se sostienen, mantienen unidos gracias a otro(s) elementos. Si se quita este elemento importante la estructura se derrumba. 

![Dependencia](https://i.pinimg.com/736x/97/4b/4a/974b4a071df7ff5953632b166e697c31.jpg)  

## ¿Cómo podemos llevar esta problemática a acciones?  
### __Para después llevarlas a coding__   
° Sujeto A le entrega mucha carga a sujeto B;  
 - Mientras más carga sujeto A le entrega a B, sujeto A se siente más aliviado, liviano, tranquilo. __Importante señalar que sujeto A puede representar tanto a una sola persona, digase un hije, mascota, persona mayor, etc, como también puede ser la sociedad. Tomando en cuenta la información entregada podemos ver que toda una sociedad se sostiene gracias a las personas que hacen un trabajo invisible no remunerado.__
 - Mientras más carga recibe sujeto B, más chiquito se va haciendo, cambia de color, va desapareciendo. Cada vez pierde más su espacio, A se apodera de todo el entorno.

#### Primer boceto del storyboard  
![boceto](https://i.pinimg.com/736x/f3/37/eb/f337eb7ccd49b8fb3cdb826931faf40e.jpg)  

#### Ejercicios clases que me ayudaron a construir la solemne  
Creación variables propias [Ejercicio01](https://editor.p5js.org/PoliMujica/sketches/vAQgFOKSy)  
Organizar JavaScript [Ejercicio02](https://editor.p5js.org/PoliMujica/sketches/cuJXAPjTm)  
If, else if, else [Ejercicio03](https://editor.p5js.org/PoliMujica/sketches/Vw-QeAsTu)  

#### Tutorial para colisiones elementos
[youtube](https://youtu.be/EFDesKpLCG0?si=TrXL2reeb3GqreRc)

#### Cómo poner una imagen
[p5.js](https://p5js.org/reference/p5/loadImage/)  

### Código p5.js
#### sketch  
let clicks = 0;

let gravity = 0.1;
let restitution = 0.5;
let balls = []; let num = 1;


let sujetoA = {
  x: 600,
  y: 0,
};
let sujetoB = {
  x: 600,
  y: 700
};

let miFuente;
let img;

function preload() {
  miFuente = loadFont('PressStart2P-Regular.ttf');
  img = loadImage('caution.png');
}

function setup() {
  createCanvas(1200, 700);
  angleMode(DEGREES);
  
  for (let i=0; i<num; i++){
    let x = random(0,width/2);
    let y = random(-300,-100);
    let r = random(30,70);
    balls.push(new Ball(x,y,r));
  }
  
}

function draw() {
  
       for (let i=0; i<balls.length; i++){
    for (let j=i+1; j<balls.length; j++){
      let ballA = balls[i];
      let ballB = balls[j];
      ballA.collide(ballB);
    }
  }
  
  for (let i=0; i<balls.length; i++){
     balls[i].update();
     balls[i].display();
  }
  
}

function mousePressed() {
 clicks++;
  
  let x = mouseX;
  let y = mouseY;
  let r = random(30,70);
  balls.push(new Ball(x,y,r));
  
  push();  
  if (clicks <= 10){
  textSize(32);
  fill(0);
  noStroke(); textFont("miFuente");
  text('"ESTAMOS MUY CANSADXS!!"\n Haz click y dale el trabajo a la personita de abajo\n click to continue',40,50);
  }else if (clicks <=20){
  textSize(32);
  fill(0);
  noStroke();
  //textFont("Press+Start+2P");
  text('"TENGO MENOS TRABAJO, QUÉ BIEN!!"\n Haz click y sigue dándole trabajo\n press to continue',40,50);
  } else {
  textSize(32);
  fill(0);
  noStroke();
  text('Tenemos menos trabajo,\n pero a costo de haber explotado\n a la otra persona',100,50);
  }
  pop();
 
  if(clicks <= 10){

   // Situación 1
  background(205, 250, 226,50);
  
    
  noStroke();
  fill(189, 6, 0);
  ellipse(sujetoA.x,sujetoA.y,100,100)
  stroke(0,0,0);
  strokeWeight(5);
  noFill();
  arc(600, 30, 50, 20, 180, 360);
  
  
  noStroke();
  fill(150, 230, 242);
  ellipse(sujetoB.x,sujetoB.y,800,800);
  stroke(104, 232, 126);
  strokeWeight(10);
  noFill();
  arc(600, 580, 200, 170, 360, 180);
  arc(500, 450, 100, 80, 360, 180);
  arc(700, 450, 100, 80, 360, 180);
  } else if(clicks <= 20){
 // Situación 2
   background(20, 48, 76);
     
  noStroke();
  fill(235, 92, 12);
  ellipse(sujetoA.x,sujetoA.y,500,500)
  stroke(0,0,0);
  strokeWeight(5);
  noFill();
  arc(600, 130, 100, 40, 360, 180);
     
  noStroke();
  fill(204, 222, 55,200);
  ellipse(sujetoB.x,sujetoB.y,300,300);
  stroke(26, 69, 22);
  strokeWeight(10);
  noFill();
  arc(600, 690, 50, 30, 230, 320);
  arc(550, 610, 70, 40, 40, 130);
  arc(650, 610, 70, 40, 40, 130);
    
  } else{
// Situación 3
    background(255,0,0);
  
  noStroke();
  fill(38, 255, 67);
  ellipse(sujetoA.x,sujetoA.y,1000,1000)
  stroke(0,0,0);
  strokeWeight(10);
  noFill();
  arc(600, 250, 400, 250, 360, 180);
     
  noStroke();
  fill(6, 8, 82,100);
  ellipse(sujetoB.x,sujetoB.y,100,100);
  /*
  stroke(104, 232, 126);
  strokeWeight(10);
  noFill();
  arc(600, 670, 100, 80, 230, 320);
  arc(500, 550, 100, 80, 40, 130);
  arc(700, 550, 100, 80, 40, 130);
  */
    
    image (img,600,600);
  } 
}

#### Clase  
lass Ball {
  constructor(x, y,r){
  this.pos = createVector(x,y);
  this.vel = p5.Vector.random2D();
  this.vel.mult(random(2,4));
  //this.vel = createVector (0,0);
  this.acc = createVector(0, gravity);
  this.r = r;
    this.mass = this.r * this.r;
    
    this.sleep = false;
  }
  
  update(){
    if (!this.sleep){
      this.vel.add(this.acc);
      this.pos.add(this.vel);
      this.bounds();
      
      if(this.pos.y + this.r >= height && abs(this.vel.y) < 0.5 && abs(this.vel.x) < 0.1){
     this.vel.set(0,0);
     this.pos.y = height - this.r;
     this.sleep = true; 
      }
    }
   
  }
  
  bounds(){
    if (this.pos.y + this.r >= height){
      this.pos.y = height - this.r;
      this.vel.y *= -restitution;
    } else if (this.pos.y - this.r <= 0){
      this.pos.y = this.r;
      this.vel.y *= -restitution;
    }
    
    if (this.pos.x + this.r >= width){
      this.pos.x = width - this.r;
      this.vel.x *= -restitution;
    } else if (this.pos.x - this.r <= 0){
      this.pos.x = this.r;
      this.vel.x *= -restitution;
    }
  }
  
  display(){
    fill(random(255));
    ellipse(this.pos.x, this.pos.y, this.r*2);
  }
  
  collide(other){
  let distAB = p5.Vector.sub(other.pos, this.pos);
  let distABMag = distAB.mag();
  let minDist = this.r + other.r;
  
  if (distABMag < minDist){
    let overlap = minDist - distABMag;
    let n = distAB.copy().normalize();
    // Corregir posiciones para que no se sobrepongan
    let correction = p5.Vector.mult(n, overlap/2);
    this.pos.sub(correction);
    other.pos.add(correction);
    
    // Encontrar nuevas velocidades
    // Encontrar una velocidad relativa y velocidad de separación
    let relativeVel = p5.Vector.sub(other.vel, this.vel);
    let separationVel = relativeVel.dot(n);
    if (separationVel < 0){
      let e = restitution;
      let invMassA = 1 / this.mass;
      let invMassB = 1 / other.mass
      
      let j = -(1 + e) * separationVel / (invMassA + invMassB);
      let impulse = p5.Vector.mult(n, j);
      let impulseA = p5.Vector.mult(impulse, invMassA);
      let impulseB = p5.Vector.mult(impulse, invMassB);
      
      this.vel.sub(impulseA);
      other.vel.add(impulseB);
    }
  } 
  }
  
}

### Diagrama de flujo  
![diagrama](https://i.pinimg.com/736x/e6/af/89/e6af8956f77e193631a4f0f2a80fbaf5.jpg)  

## Enlace a solemne en p5.js  
[p5.js](https://editor.p5js.org/IsaCarvacho/sketches/1LIC-Lk2x)  

#### Errores que no pude solucionar  
1. Seleccionar tipografía (Intenté poner una tipo juego antiguo)
2.  Insertar imagen
3.  Texto de última escena no aparece
4. A pesar de que los círculos que colisionan los intenté sacar de la función draw, cuando los sacaba desaparecían. Por lo que tuve que dejarlo en draw y quedan con estelas que no dejan el mejor efecto estético al trabajo.
5. Elementos como map(), translate y otros no los alcancé a poner en el trabajo. 
