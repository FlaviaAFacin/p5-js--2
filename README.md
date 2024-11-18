# p5-js--2<!DOCTYPE html>
<html lang="en">
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.4/p5.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.4/addons/p5.sound.min.js"></script>
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />

  </head>
  <body>
    <main>
    </main>
    <script src="sketch.js"></script>
  </body>
</html>

let palavra//variavel palavra

function setup(){//preparar a tela
  createCanvas(700, 400)//cria canva
  
  palavra = palavraAleatoria();//determina palavrasa aleatórias
  
}

function palavraAleatoria(){//função palavraAleatoria
  let palavras = ["Trono de Vidro", "Razão do Amor", "De Lukov com Amor", "É Assim que Acaba"];//determina as palavras
  return random(palavras);//zera palavras
}
function inicializaCores() {//inicializar cores
  background("pink")// cenário rosa
  fill ("magenta")//cor da letra
  textSize (64);//tamanho da letra
  textAlign (CENTER, CENTER);//posição da palavra
}
  
function palavraParcial(minimo, maximo){//função palavraParcial
   let quantidade = map(mouseX, minimo, maximo, 1, palavra.length);//quantidade de letras que vai utilizar
  let parcial = palavra.substring(0, quantidade);//corresponde a um pedaço da palavra
  return parcial;//
}


function draw() {// desenhar
  inicializaCores();// inicializa cores
  
  let texto = palavraParcial(0, width);//variável texto=palvraParcial
  text(texto, 200, 200);//posição do texto
  
}

function livrosParaFugirDaRealidade(nome, gênero){
  
}
