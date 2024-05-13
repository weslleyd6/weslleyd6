//variáveis de bolinha
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;
let raio = diametro /2;

//velocidade da bolinha
let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;
//variáveis da raquete
let xRaquete = 5;
let yRaquete = 150;
let RaqueteComprimento = 10;
let RaqueteAltura = 90;

function setup(){
    createCanvas(600, 400);
}
function setup(){
  createCanvas(400, 400);
}

function draw(){
  background(0);
  mostrarBolinha();
  movimentaBolinha();
  verificaColisaoBorda();
  mostraRaquete();
  movimentaMinhaRaquete();
}
function mostrarBolinha(){
  circle(xBolinha, yBolinha, diametro);
}
function movimentaBolinha(){
 xBolinha += velocidadeXBolinha;
 yBolinha += velocidadeYBolinha;
}
function verificaColisaoBorda(){
  if(xBolinha > width|| xBolinha - raio < 0){
    velocidadeXBolinha*= -1;
  }
  if (yBolinha > height || yBolinha - raio < 0){
    velocidadeYBolinha*= -1;
  }
}
function mostraRaquete(){
  rect(xRaquete, yRaquete, 
RaqueteComprimento, RaqueteAltura);
}
function movimentaMinhaRaquete(){
  if(keyIsDown(UP_ARROW)) {
    yRaquete -= 10;
  }
  if(keyIsDown(DOWN_ARROW)) {
    yRaquete += 10;
  }
}
