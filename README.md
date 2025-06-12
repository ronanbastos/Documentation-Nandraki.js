&lt;h1 align="center"> &lt;img src="[link suspeito removido]" alt="mascote" border="0">&lt;/h1>

Nandraki.js
Projetos prontos: Demonstrações no GitHub

Nandraki.js é uma biblioteca JavaScript que fornece recursos para a criação de jogos 2D em HTML5 Canvas. É uma ferramenta leve e simples de usar que pode ser facilmente adicionada a qualquer projeto. "Nandraki" contém alguns métodos estáticos para criação e movimento de elementos gráficos (sprites) e elementos de interface do usuário (UI).

Principais Recursos
Criação de sprites animados: Permite que você crie personagens, inimigos e objetos animados para seu jogo.
Controles de teclado: Possui um sistema de detecção de teclas que permite criar controles para seu jogo, como movimentação de personagens e ações.
Loop de jogo: Com o Nandraki.js, você pode criar um loop de jogo que atualiza a tela a cada quadro, criando uma experiência fluida e interativa.
Gerenciamento de recursos: Permite que você gerencie seus recursos de jogo, como imagens, sons e fontes, de forma simples e organizada.
Exemplo de Configuração Inicial
HTML

<!DOCTYPE html>
<html>
<head>
    <script src="https://unpkg.com/nandraki@2.1.0/nandraki.js"></script>
</head>
<body>
    <script>
        Nandraki.create_ui("text_id", "[hello world]");
        
        myjogo = {
            start: function() {
                // Nandraki.create_ui("text_id","hello world");
            },
        };

        fps = 60;
        game.update(myjogo.start, fps);
    </script>
</body>
</html>
Exemplo Básico de Jogo
JavaScript

// Inicia o canvas com 800x500 pixels
game.canvas_start("canvas", 800, 500);

// Obtém o contexto 2D do canvas
game.context("canvas");

// Cria um sprite animado
player = game.frame_sprite("player", "player.png", Nandraki, 64, 64, 0, 0, 0, 5, 7);

function jogo() {
    // Limpa o canvas a cada quadro
    Nandraki.clearRect(0, 0, canvas.width, canvas.height);

    // Renderiza o sprite na posição (x, y)
    game.render_sprite(player, Nandraki, x, y);

    // Prepara para o próximo quadro
    game.rest(jogo, canvas);
}

// Inicia o loop do jogo
game.loop(jogo, canvas);
Documentação da API (Funções)
Classe Nandraki (Métodos Estáticos)
create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top): Cria um sprite com várias camadas de imagens, com um ID e posição especificados.
move_obj(id, left, top, fixed): Move um sprite ou elemento gráfico para uma posição. O parâmetro fixed especifica se a posição é fixa ou absoluta.
create_ui(id, txt, cor): Cria um elemento de interface do usuário com ID, texto e cor especificados.
move_ui(id, left, top, fixed): Move um elemento de UI para uma posição. O parâmetro fixed especifica se a posição é fixa ou absoluta.
Funções do Objeto game
canvas_start(id, width, height): Cria um elemento <canvas> com ID, largura e altura definidos.
canvas_text(text, font, cor, x, y): Desenha texto no canvas.
context(id): Retorna o contexto de desenho 2D do canvas.
canvas_arc(x, y, font, b, p): Desenha um arco no canvas.
canvas_rect(x, y, height, width): Desenha um retângulo no canvas.
canvas_click(func): Adiciona um ouvinte de clique ao canvas.
obj(): Cria e retorna um novo objeto vazio.
canvas_clear(): Limpa o conteúdo do canvas.
background_add(id, image_url): Adiciona uma imagem de fundo a um elemento.
reload(): Recarrega a página atual.
stop_interval(intervalId): Interrompe um setInterval.
start_interval(func, time): Inicia um setInterval.
stop_time(timeoutId): Interrompe um setTimeout.
get_tecla(): Exibe no console o código da tecla pressionada.
click_som(id, link): Reproduz um som quando um elemento é clicado.
click(id, func): Executa uma função quando um elemento é clicado.
click_target(element, func): Executa uma função quando um elemento HTML específico é clicado.
start_som(link): Reproduz um arquivo de áudio.
time_som(link, ms): Reproduz um áudio após um tempo especificado.
spawn_sprite(id, src, left, top): Cria uma nova imagem (sprite) na página.
set_src(id, src): Define a fonte (src) de uma imagem.
img_size(id, width, height): Define o tamanho de uma imagem.
fixed(id): Define a posição de uma imagem como fixed.
start_time(func, time): Executa uma função em intervalos regulares.
bd_save(key, value): Salva um valor no localStorage.
bd_load(key): Carrega um valor do localStorage.
bd_remove(key): Remove um valor do localStorage.
bd_clear(): Limpa todo o localStorage.
img_frame(id, width, height, startFrame, endFrame, frameRate): Define uma imagem como um sprite animado.
animar_left(id, min, max): Anima um elemento horizontalmente.
animar_top(id, min, max): Anima um elemento verticalmente.
pixeled(id): Renderiza o elemento com image-rendering: pixelated.
jump_force(id, min, max): Anima um elemento para pular.
get_mouse_x(): Retorna a posição X do mouse.
get_mouse_y(): Retorna a posição Y do mouse.
fonte_size(id, size): Define o font-size de um elemento.
color(id, color): Define a cor do texto de um elemento.
get_left(id): Retorna a posição left de um elemento.
get_tx(id): Retorna a posição X de um elemento com base na transformação CSS.
get_ty(id): Retorna a posição Y de um elemento com base na transformação CSS.
get_top(id): Retorna a posição top de um elemento.
moveX_rest(id, position, rest): Move um elemento horizontalmente até uma posição.
speed_row(id, speed, startPosition): Move um elemento horizontalmente com velocidade.
moveXD(id): Move um elemento para a direita.
moveXE(id): Move um elemento para a esquerda.
timeXD(id, delay): Move um elemento para a direita com atraso.
timeXE(id, delay): Move um elemento para a esquerda com atraso.
force_obj(id, x, y, rotate): Move um elemento e opcionalmente o rotaciona.
scaleX(id, value): Define a escala de um elemento no eixo X.
load(url): Carrega uma nova página.
load_time(url, time): Carrega uma nova página após um tempo.
hover_mouse(id, func): Adiciona um ouvinte de evento mouseover.
move_mouse(id): Adiciona funcionalidade de arrastar com o mouse.
touch_start(id, func): Adiciona um ouvinte de evento touchstart.
touch_end(id, func): Adiciona um ouvinte de evento touchend.
ative_touch(value): Define a propriedade touch-action.
transform(id, x, y, rotate): Define a propriedade transform de um elemento.
wrap_text(id): Define word-wrap: break-word.
touch_long(id, func, t): Adiciona um ouvinte para um toque longo.
move_touch(id): Adiciona funcionalidade de arrastar por toque.
move_touch_pro(id, id_container): Adiciona arrastar por toque limitado a um contêiner.
block_all(selector): Define display: block para todos os elementos correspondentes.
random_m(max, min, offset): Retorna um número aleatório em um intervalo.
random_mf(max): Retorna um número inteiro aleatório entre 1 e max.
log_down(func): Adiciona um ouvinte de evento keydown.
log_up(func): Adiciona um ouvinte de evento keyup.
opacity(id, value): Define a opacidade de um elemento.
type_curso(id, cursorType): Define o tipo de cursor de um elemento.
get_input(id): Obtém o valor de um campo de entrada.
fixed_body(zoom): Cria um efeito de tela fixa com zoom.
camera(aspecto, x, y, limitX, limitY): Move a janela do navegador (câmera 2D).
fpsFrame(obj, func, fps): Limita os frames por segundo de uma animação.
frame_sprite(...): Cria um objeto sprite com propriedades de animação.
update_sprite(spriteObject): Atualiza o índice do quadro do sprite.
render_sprite(spriteObject, context, x, y): Renderiza e atualiza um sprite no canvas.
img_canvas(...): Desenha uma imagem em um contexto de canvas.
obj_in_obj(parentId, childId): Adiciona um objeto filho a um objeto pai no HTML.
remove_class(id, className): Remove uma classe CSS de um elemento.
get_window_w(): Retorna a largura da janela.
get_window_h(): Retorna a altura da janela.
responsive_img(id): Redimensiona uma imagem de acordo com a janela.
move_responsive(id, x, y): Move um objeto de forma responsiva.
animar_obj(id, cssAnimation): Anima um objeto HTML usando CSS.
text_bot(id, text, speed): Cria um efeito de digitação.
touchpad(...): Cria um touchpad virtual para dispositivos móveis.
get_text(id): Obtém o texto de um elemento.
set_text(id, text): Define o texto de um elemento.
edite_text(id, newText): Edita o texto de um elemento.
modal(...): Cria um modal personalizado.
gravity(obj, environment): Implementa física de gravidade.
force_gravity(obj, environment): Implementa a força da gravidade.
jump(obj): Implementa a mecânica de saltos.
Rel_distanica(obj1, obj2): Calcula a distância relativa entre dois objetos.
colidir_obj(obj1, obj2): Verifica se dois objetos colidiram.
colidir_aq(obj, area): Verifica se um objeto está dentro de uma área.
right_check(obj1, obj2): Verifica se um objeto está à direita de outro.
top_up_check(obj1, obj2): Verifica se um objeto está acima de outro.
colidir_force_r(id1, id2, check_contato): Verifica colisão da direita de id1 com a esquerda de id2.
colidir_force_l(id1, id2, check_contato): Verifica colisão da esquerda de id1 com a direita de id2.
colidir(rect1, rect2): Verifica se dois retângulos colidiram.
coord(id): Retorna as coordenadas de um retângulo (getBoundingClientRect).
rest(callback): Referência a requestAnimationFrame.
loop(callback): Referência a requestAnimationFrame.
update(gameFunction, fps): Atualiza o jogo em um intervalo de tempo (setInterval).
Exemplo 1: Criar Objeto com Classe Nandraki
Passo 1: Defina uma nova classe chamada Nandraki.
Passo 2: Dentro da classe, defina o método constructor.
Passo 3: Atribua os parâmetros às propriedades correspondentes usando this.
Passo 4: Defina a propriedade body como o elemento HTML correspondente.
Passo 5: Instancie o objeto usando a palavra-chave new.

JavaScript

class Nandraki {
    constructor(id, vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame) {
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
        this.body = document.getElementById(this.id); // Corrigido para usar this.id
    }
}
Todos os Métodos da Classe Nandraki.js
JavaScript

// Criação de Sprites e UI
Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top);
Nandraki.create_ui(id, txt, cor);
Nandraki.move_obj(id, left, top, fixed);

// Exemplo de criação de sprite para um jogador
Nandraki.create_sprite(player.id, 5, player.img.parado, player.img.andando, player.img.pulo, player.img.atacando01, player.img.atacando02, 64, 64, 15, 32, 250, 250);

// Criação e manipulação de caixas de colisão (hitbox)
Nandraki.create_box("player", 20, 20, 0, 0, "block");
Nandraki.move_obj("box_player", game.get_tx(player.id) + 20, game.get_ty(player.id) + 25, false);
Nandraki.ative_box("box_player", false);
Sobre Draki3D
1. Classe ThreeCore
A ThreeCore gerencia o núcleo da cena 3D (ambiente, câmera, renderizador) e usa o padrão Singleton para garantir que apenas uma instância seja criada.

Construtor (constructor):
Cena 3D: Onde todos os objetos 3D são colocados.
Câmera: Usa uma câmera de perspectiva para simular a visão 3D.
Renderizador: O motor que desenha a cena. alpha: true permite um fundo transparente.
Singleton: ThreeCore.instance = this garante que apenas uma instância da classe exista.
Métodos:
init(container): Inicializa a cena, adiciona o renderizador à página e inicia o loop de animação.
animate(): Chamado repetidamente via requestAnimationFrame para renderizar a cena a cada quadro, permitindo animação contínua.
2. Classe ThreeFactory
Responsável por criar objetos 3D fundamentais (luzes, cubos). É um exemplo do padrão Abstract Factory.

Métodos:
createLight(): Cria uma luz pontual.
createCube(): Cria um cubo 3D verde.
createCamera(): Cria uma câmera de perspectiva.
3. Classe EntityBuilder
Implementa o padrão Builder, permitindo construir entidades complexas de forma flexível.

Métodos:
addMesh(mesh): Adiciona uma malha 3D (como um cubo) à entidade.
setPosition(x, y, z): Define a posição da entidade no espaço 3D.
build(): Finaliza a construção e retorna a entidade 3D.
4. Classe PrototypeFactory
Segue o padrão Prototype, permitindo registrar e clonar objetos 3D para economizar recursos.

Métodos:
register(name, object3D): Registra um objeto 3D para que possa ser clonado.
clone(name): Clona um objeto registrado, retornando uma cópia exata.
5. Classe Game
Utiliza a ThreeFactory para criar objetos de forma simplificada.

Objeto de Mapeamento: Um objeto objects mapeia tipos ('cube', 'camera', 'light') para suas instâncias criadas pela ThreeFactory.
Método create(type): Retorna o objeto correspondente ao type solicitado. Lança um erro se o tipo for desconhecido. Isso torna a criação de objetos simples e eficiente.
