<h1 align="center">
  <img src="https://i.ibb.co/n3BMNKM/logo.png" alt="mascote" border="0">
</h1>
<br>


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


<br>

<p>Projetos prontos: <a href="https://github.com/ronanbastos/Nandraki.js/tree/main/Demonstration">https://github.com/ronanbastos/Nandraki.js/tree/main/Demonstration</a></p>

<p>"Nandraki" com tem alguns métodos estáticos para criação e movimento de elementos gráficos (sprites) e elementos de interface do usuário (UI).</p>

<h2>Métodos da Classe</h2>

<p>O construtor recebe vários parâmetros e os atribui às propriedades correspondentes da instância da classe.</p>

<h3>Métodos Estáticos</h3>

<ul>
  <li><strong>create_sprite</strong>: Usado para criar um sprite com várias camadas de imagens.</li>
  <li><strong>move_obj</strong>: Usado para mover um sprite ou outro elemento gráfico.</li>
  <li><strong>create_ui</strong>: Usado para criar um elemento de interface do usuário.</li>
  <li><strong>move_ui</strong>: Usado para mover um elemento de interface do usuário.</li>
</ul>

<h2>Sobre Nandraki.js</h2>

<p>Nandraki.js é uma biblioteca JavaScript que fornece recursos para criação de jogos 2D em HTML5 Canvas. Ele é uma ferramenta leve e simples de usar que pode ser facilmente adicionada a qualquer projeto.</p>

<h3>Principais Recursos</h3>

<ul>
  <li>Criação de sprites animados</li>
  <li>Controles de teclado</li>
  <li>Loop de jogo</li>
  <li>Gerenciamento de recursos</li>
</ul>

<h3>Exemplo Básico</h3>

<pre><code>game.canvas_start("canvas",800,500)	
game.context("canvas")
player = game.frame_sprite("player","player.png",Nandraki,64,64,0,0,0,5,7)

function jogo(){
  Nandraki.clearRect(0, 0, canvas.width, canvas.height);
  game.render_sprite(player,Nandraki,x,y)
  game.rest(jogo,canvas);
}

game.loop(jogo,canvas)</code></pre>

<h2>Funções Principais</h2>

<ul>
  <li><strong>canvas_start(id, width, height)</strong>: Cria um elemento canvas</li>
  <li><strong>canvas_text(text, font, cor, x, y)</strong>: Desenha texto no canvas</li>
  <li><strong>context(id)</strong>: Retorna o contexto de desenho</li>
  <li><strong>canvas_arc(x, y, font, b, p)</strong>: Desenha um arco</li>
  <li><strong>canvas_rect(x, y, height, width)</strong>: Desenha um retângulo</li>
</ul>

<h2>Exemplo com Classe Nandraki</h2>

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

<h2>Sobre Draki3D</h2>

<h3>1. Classe ThreeCore</h3>
<p>A ThreeCore é a classe que gerencia o núcleo da cena 3D, como o ambiente, a câmera e o renderizador.</p>

<h3>2. Classe ThreeFactory</h3>
<p>Responsável por criar os objetos 3D fundamentais, como luzes, cubos e câmeras.</p>

<h3>3. Classe EntityBuilder</h3>
<p>Implementação do padrão Builder para construir entidades compostas de forma flexível.</p>

<h3>4. Classe PrototypeFactory</h3>
<p>Seguindo o padrão Prototype, permite registrar e clonar objetos 3D.</p>

<h3>5. Classe Game</h3>
<p>Utiliza a ThreeFactory para criar objetos de forma simplificada.</p>
