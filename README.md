<h1 align="center">
  <img src="https://i.ibb.co/n3BMNKM/logo.png" alt="mascote" border="0">
</h1>
<br>
<code>
<!DOCTYPE html>
<html>
<head>
  <script src="https://unpkg.com/nandraki@2.1.0/nandraki.js"></script>
</head>
<body>
  <script>
    Nandraki.create_ui("text_id","[hello world]")
    myjogo = {
      start: function(){
        // Nandraki.create_ui("text_id","hello world")	
      },
    }
    fps=60;	
    game.update(myjogo.start,fps);  
  </script>
</body>
</html>
</code>
<br>

<p>Projetos prontos: <a href="https://github.com/ronanbastos/Nandraki.js/tree/main/Demonstration">https://github.com/ronanbastos/Nandraki.js/tree/main/Demonstration</a></p>

<p>"Nandraki" com tem alguns métodos estáticos para criação e movimento de elementos gráficos (sprites) e elementos de interface do usuário (UI).</p>

<h2>Métodos da classe:</h2>

<p>O construtor recebe vários parâmetros e os atribui às propriedades correspondentes da instância da classe.</p>

<p>O método estático "create_sprite" é usado para criar um sprite com várias camadas de imagens. O número de camadas é especificado pelo parâmetro "camadas", e as imagens são fornecidas pelos parâmetros "img1", "img2", "img3", "img4" e "img5". O sprite é criado com um ID especificado pelo parâmetro "id" e uma posição especificada pelos parâmetros "left" e "top".</p>

<p>O método estático "move_obj" é usado para mover um sprite ou outro elemento gráfico com um ID especificado pelo parâmetro "id" para uma posição especificada pelos parâmetros "left" e "top". O parâmetro "fixed" é usado para especificar se o elemento deve ser movido com posição fixa ou absoluta.</p>

<p>O método estático "create_ui" é usado para criar um elemento de interface do usuário com um ID especificado pelo parâmetro "id", um texto especificado pelo parâmetro "txt" e uma cor especificada pelo parâmetro "cor".</p>

<p>O método estático "move_ui" é usado para mover um elemento de interface do usuário com um ID especificado pelo parâmetro "id" para uma posição especificada pelos parâmetros "left" e "top". O parâmetro "fixed" é usado para especificar se o elemento deve ser movido com posição fixa ou absoluta.</p>

<h2>Sobre Nandraki.js</h2>

<p>Nandraki.js é uma biblioteca JavaScript que fornece recursos para criação de jogos 2D em HTML5 Canvas. Ele é uma ferramenta leve e simples de usar que pode ser facilmente adicionada a qualquer projeto.</p>

<h3>Principais recursos:</h3>
<ul>
  <li>Criação de sprites animados - permitindo que você crie personagens, inimigos e objetos animados para seu jogo.</li>
  <li>Controles de teclado - o Nandraki.js tem um sistema de detecção de teclas que permite criar controles para seu jogo, como movimentação de personagens e ações.</li>
  <li>Loop de jogo - com o Nandraki.js, você pode criar um loop de jogo que atualiza a tela a cada quadro, criando uma experiência fluida e interativa para o usuário.</li>
  <li>Gerenciamento de recursos - Nandraki.js permite que você gerencie seus recursos de jogo, como imagens, sons e fontes, de forma simples e organizada.</li>
</ul>

<p>Para começar a usar o Nandraki.js, basta baixar a biblioteca e incluí-la em sua página HTML. A partir daí, você pode começar a criar seus sprites, adicionar controles de teclado e criar um loop de jogo.</p>

<h3>Exemplo básico de código:</h3>
<pre><code>game.canvas_start("canvas",800,500)	
game.context("canvas")
player = game.frame_sprite("player","player.png",Nandraki,64,64,0,0,0,5,7)

function jogo(){
  Nandraki.clearRect(0, 0, canvas.width, canvas.height);
  game.render_sprite(player,Nandraki,x,y)
  game.rest(jogo,canvas);
}

game.loop(jogo,canvas)</code></pre>

<h2>Funções disponíveis:</h2>

<h3>Funções básicas:</h3>
<ul>
  <li>canvas_start(id, width, height): cria um elemento de canvas HTML com o ID especificado e largura e altura definidas.</li>
  <li>canvas_text(text, font, cor, x, y): desenha um texto na posição (x, y) do canvas com a fonte e cor especificadas.</li>
  <li>context(id): retorna o contexto de desenho 2D do canvas HTML com o ID especificado.</li>
  <li>canvas_arc(x, y, font, b, p): desenha um arco no canvas na posição (x, y) com o raio definido por font.</li>
  <li>canvas_rect(x, y, height, width): desenha um retângulo no canvas na posição (x, y) com a altura e largura especificadas.</li>
</ul>

<h3>Funções avançadas:</h3>
<ul>
  <li>fpsFrame(obj, func, fps): limita os frames por segundo de uma animação.</li>
  <li>frame_sprite(): cria um objeto sprite com propriedades de animação.</li>
  <li>update_sprite: atualiza o sprite de uma imagem.</li>
  <li>render_sprite: renderiza o sprite de uma imagem em um contexto.</li>
</ul>

<h2>Exemplo 1: Criar objeto com Classe Nandraki</h2>
<pre><code>class Nandraki {
  constructor(id,vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame){
    this.id = id;
    this.vida = vida;
    this.gravidade = gravidade;
    this.velocidade = velocidade;
    this.massa = massa;
    this.di = di;
    this.up = up;
    this.mirror = mirror;
    this.anim = anim;
    this.jump = jump;
    this.frame = frame;
    this.body = document.getElementById(obj.id);
  }
}</code></pre>

<h3>Todos métodos da class Nandraki.js:</h3>
<pre><code>Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)	
Nandraki.create_ui(id,txt,cor)
Nandraki.move_obj(id,left,top,fixed)
Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)	
constructor(id,vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame)
Nandraki.create_ui(id,txt,cor)
Nandraki.move_obj(id,left,top,fixed)
Nandraki.create_sprite(player.id,5,player.img.parado,player.img.andando,player.img.pulo,player.img.atacando01,player.img.atacando02,64,64,15,32,250,250)

Nandraki.create_box("player",20,20,0,0,"block")
Nandraki.move_obj("box_player",game.get_tx(player.id)+20,game.get_ty(player.id)+25,false)
Nandraki.ative_box("box_player",false)</code></pre>

<h2>Sobre Draki3D</h2>

<h3>1. Classe ThreeCore</h3>
<p>A ThreeCore é a classe que gerencia o núcleo da cena 3D, como o ambiente, a câmera e o renderizador. Ela também garante que apenas uma instância de ThreeCore seja criada, usando o padrão Singleton.</p>

<h4>Métodos:</h4>
<ul>
  <li>init(container): Inicializa a cena, adiciona o renderizador ao container da página HTML e começa o loop de animação.</li>
  <li>animate(): Este método é chamado repetidamente através de requestAnimationFrame.</li>
</ul>

<h3>2. Classe ThreeFactory</h3>
<p>A ThreeFactory é responsável por criar os objetos 3D fundamentais, como luzes, cubos e câmeras.</p>

<h4>Métodos:</h4>
<ul>
  <li>createLight(): Cria uma luz pontual.</li>
  <li>createCube(): Cria um cubo 3D com uma cor verde.</li>
  <li>createCamera(): Cria uma câmera de perspectiva.</li>
</ul>

<h3>3. Classe EntityBuilder</h3>
<p>A EntityBuilder é uma implementação do padrão Builder. Ela permite construir entidades compostas de forma mais flexível.</p>

<h4>Métodos:</h4>
<ul>
  <li>addMesh(mesh): Adiciona um mesh à entidade.</li>
  <li>setPosition(x, y, z): Define a posição da entidade no espaço 3D.</li>
  <li>build(): Finaliza a construção e retorna a entidade 3D.</li>
</ul>

<h3>4. Classe PrototypeFactory</h3>
<p>A PrototypeFactory segue o padrão Prototype. Ela permite registrar e clonar objetos 3D.</p>

<h4>Métodos:</h4>
<ul>
  <li>register(name, object3D): Registra um objeto 3D com um nome.</li>
  <li>clone(name): Clona um objeto registrado anteriormente.</li>
</ul>

<h3>5. Classe Game</h3>
<p>A classe Game utiliza a ThreeFactory para criar objetos de forma simplificada.</p>

<h4>Método:</h4>
<ul>
  <li>create(type): Cria os objetos 3D usando a ThreeFactory.</li>
</ul>

<h4>Resumo de como funciona:</h4>
<ul>
  <li>ThreeCore gerencia o ciclo de vida da cena, a câmera e o renderizador.</li>
  <li>ThreeFactory cria objetos 3D, como luzes, cubos e câmeras.</li>
  <li>EntityBuilder ajuda a construir entidades 3D compostas.</li>
  <li>PrototypeFactory permite clonar objetos registrados.</li>
  <li>Game é a interface simplificada para criar objetos e interagir com a cena 3D.</li>
</ul>
