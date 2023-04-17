Este é um código em JavaScript que define uma classe chamada "Nandraki" com alguns métodos estáticos para criação e movimento de elementos gráficos (sprites) e elementos de interface do usuário (UI).

Aqui está uma breve explicação dos métodos da classe:

    O construtor recebe vários parâmetros e os atribui às propriedades correspondentes da instância da classe.
    O método estático "create_sprite" é usado para criar um sprite com várias camadas de imagens. O número de camadas é especificado pelo parâmetro "camadas", e as imagens são fornecidas pelos parâmetros "img1", "img2", "img3", "img4" e "img5". O sprite é criado com um ID especificado pelo parâmetro "id" e uma posição especificada pelos parâmetros "left" e "top".
    O método estático "move_obj" é usado para mover um sprite ou outro elemento gráfico com um ID especificado pelo parâmetro "id" para uma posição especificada pelos parâmetros "left" e "top". O parâmetro "fixed" é usado para especificar se o elemento deve ser movido com posição fixa ou absoluta.
    O método estático "create_ui" é usado para criar um elemento de interface do usuário com um ID especificado pelo parâmetro "id", um texto especificado pelo parâmetro "txt" e uma cor especificada pelo parâmetro "cor".
    O método estático "move_ui" é usado para mover um elemento de interface do usuário com um ID especificado pelo parâmetro "id" para uma posição especificada pelos parâmetros "left" e "top". O parâmetro "fixed" é usado para especificar se o elemento deve ser movido com posição fixa ou absoluta.
    
Nandraki.js é uma biblioteca JavaScript que fornece recursos para criação de jogos 2D em HTML5 Canvas. Ele é uma ferramenta leve e simples de usar que pode ser facilmente adicionada a qualquer projeto.

Os principais recursos do Nandraki.js incluem:

    Criação de sprites animados - permitindo que você crie personagens, inimigos e objetos animados para seu jogo.

    Controles de teclado - o Nandraki.js tem um sistema de detecção de teclas que permite criar controles para seu jogo, como movimentação de personagens e ações.

    Loop de jogo - com o Nandraki.js, você pode criar um loop de jogo que atualiza a tela a cada quadro, criando uma experiência fluida e interativa para o usuário.

    Gerenciamento de recursos - Nandraki.js permite que você gerencie seus recursos de jogo, como imagens, sons e fontes, de forma simples e organizada.

Para começar a usar o Nandraki.js, basta baixar a biblioteca e incluí-la em sua página HTML. A partir daí, você pode começar a criar seus sprites, adicionar controles de teclado e criar um loop de jogo.

Aqui está um exemplo básico de código usando Nandraki.js:


	game.canvas_start("canvas",800,500)	
	game.context("canvas")

	player = game.frame_sprite("player","player.png",Nandraki,64,64,0,0,0,5,7)

	function jogo(){
	   Nandraki.clearRect(0, 0, canvas.width, canvas.height);
	   game.render_sprite(player,Nandraki,x,y)
	   game.rest(jogo,canvas);
	}

	game.loop(jogo,canvas)

    canvas_start(id, width, height): cria um elemento de canvas HTML com o ID especificado e largura e altura definidas.

    canvas_text(text, font, cor, x, y): desenha um texto na posição (x, y) do canvas com a fonte e cor especificadas. Se a fonte for nula ou uma string vazia, a fonte padrão é '10px Times New Roman'.

    context(id): retorna o contexto de desenho 2D do canvas HTML com o ID especificado.

    canvas_arc(x, y, font, b, p): desenha um arco no canvas na posição (x, y) com o raio definido por font, começando no ângulo b e terminando no ângulo p.

    canvas_rect(x, y, height, width): desenha um retângulo no canvas na posição (x, y) com a altura e largura especificadas.

    canvas_click(func): adiciona um ouvinte de clique ao canvas que executa a função passada como parâmetro quando o usuário clica no canvas.
    
        obj: cria e retorna um novo objeto vazio.
    canvas_clear: limpa o conteúdo do canvas.
    background_add: adiciona uma imagem de fundo a um elemento HTML especificado por seu id.
    
    reload: recarrega a página atual.
    
    stop_interval: interrompe a execução de um intervalo de tempo especificado por seu ID.
    
    start_interval: inicia um intervalo de tempo especificado por seu ID e tempo de execução.
    
    stop_time: interrompe a execução de um temporizador especificado por seu ID.
    
    get_tecla: exibe no console o código da tecla pressionada pelo usuário.
    
    click_som: reproduz um arquivo de áudio especificado por seu link quando um elemento HTML especificado por seu ID é clicado.
    
    click: executa uma função especificada quando um elemento HTML especificado por seu ID é clicado.
    
    click_target: executa uma função especificada quando um elemento HTML específico é clicado.
    
    start_som: reproduz um arquivo de áudio especificado por seu link quando a função é chamada.
    
    time_som: reproduz um arquivo de áudio especificado por seu link após um tempo especificado em milissegundos.
    
    Função "spawn_sprite": Cria uma nova imagem (sprite) com um determinado ID, imagem, posição esquerda e posição superior na página.

    Função "set_src": Define a fonte (src) de uma imagem específica.

    Função "img_size": Define o tamanho de uma imagem específica com base em uma largura e altura fornecidas.

    Função "fixed": Define uma imagem específica como "fixa" na página, para que ela não se mova quando a página é rolada.

   Função "start_time": Executa uma determinada função em intervalos regulares com base em um tempo fornecido.

   Função "bd_save": Salva um valor em um determinado "espaço de armazenamento" no navegador, identificado por uma chave (speed).

   Função "bd_load": Carrega o valor associado a uma determinada chave (speed) de um "espaço de armazenamento" no navegador.

   Função "bd_remove": Remove um valor associado a uma determinada chave (speed) de um "espaço de armazenamento" no navegador.

   Função "bd_clear": Remove todos os valores de um determinado "espaço de armazenamento" no navegador.

   Função "img_frame": Define uma imagem como um "sprite" animado com base em uma largura e altura fornecidas, bem como um conjunto de quadros iniciais, finais e uma taxa de quadros.
   
       animar_left: anima um elemento HTML para se mover horizontalmente de uma posição mínima para uma posição máxima e depois voltar para a posição mínima.
       
    animar_top: anima um elemento HTML para se mover verticalmente de uma posição mínima para uma posição máxima e depois voltar para a posição mínima.
    
    pixeled: define o elemento HTML para ser renderizado com pixels nítidos.
    
    jump_force: anima um elemento HTML para pular de uma posição mínima para uma posição máxima.
    
    get_mouse_x: retorna a posição atual do mouse em relação ao eixo X.
    
    fonte_size: define o tamanho da fonte de um elemento HTML.
    
    color: define a cor do texto de um elemento HTML.
    
    get_mouse_y: retorna a posição atual do mouse em relação ao eixo Y.
    
    get_left: retorna a posição atual à esquerda de um elemento HTML.
    
    get_tx: retorna a posição atual à esquerda de um elemento HTML com base na transformação CSS aplicada.
    
    get_ty: retorna a posição atual no topo de um elemento HTML com base na transformação CSS aplicada.
    
    get_top: retorna a posição atual no topo de um elemento HTML.
    
    moveX_rest: move um elemento HTML horizontalmente até uma posição específica, com um espaço restante no final.
    
    speed_row: move um elemento HTML horizontalmente com uma velocidade específica após uma posição inicial.
    
    moveXD: move um elemento HTML horizontalmente para a direita.
    
    moveXE: move um elemento HTML horizontalmente para a esquerda.
    
    timeXD: move um elemento HTML horizontalmente para a direita com um atraso específico.
    
    timeXE: move um elemento HTML horizontalmente para a esquerda com um atraso específico.
    
    force_obj: move um elemento HTML para uma posição específica (especificada pelos parâmetros x e y) e o rotaciona se o parâmetro rotate for verdadeiro.
    
    scaleX: define a escala de um elemento HTML no eixo X.

    load: carrega uma nova página da web definindo o valor de window.location.href.
    
    load_time: carrega uma nova página da web após um período de tempo específico (especificado pelo parâmetro time).
    hover_mouse: adiciona um ouvinte de evento a um elemento HTML que aciona uma função quando o mouse entra no elemento.
    
    move_mouse: adiciona funcionalidade de arrastar a um elemento HTML para que ele possa ser movido ao redor da tela pelo mouse.

    touch_start: adiciona um ouvinte de evento a um elemento HTML que aciona uma função quando um evento de toque começa.

    touch_end: adiciona um ouvinte de evento a um elemento HTML que aciona uma função quando um evento de toque termina.

    ative_touch: define a ação de toque da página como "auto".

    transform: define a propriedade de transformação de um elemento HTML para um valor específico (especificado pelos parâmetros x, y e rota).

    wrap_text: define a propriedade de quebra de palavra de um elemento HTML como "break-word".

    touch_long: adiciona um ouvinte de evento a um elemento HTML que aciona uma função após um toque longo (especificado pelo parâmetro t).
    
    move_touch: adiciona funcionalidade de arrastar por toque a um elemento HTML para que ele possa ser movido ao redor da tela por toque.

    move_touch_pro: adiciona funcionalidade de arrastar por toque a um elemento HTML que é limitado a um contêiner específico (especificado pelo parâmetro id_container).
    
	    A função block_all recebe um seletor como parâmetro e seleciona todos os elementos do documento que correspondem a esse seletor. Em seguida, ela define o estilo de exibição desses elementos como "block".

	    A função random_m recebe três parâmetros: o valor máximo, o valor mínimo e o valor de deslocamento. Ela retorna um número aleatório dentro do intervalo especificado pelos valores máximo e mínimo, com um deslocamento adicional.

	A função create_go chama a função get_text do objeto game, passando a string "text" como argumento, e armazena o resultado na variável texto. Em seguida, ela chama a função random_mf do objeto game, passando os valores 1500, 5 e 5 como argumentos, e armazena o resultado na variável num. Por fim, ela chama a função create do objeto Maps, passando os argumentos "sprite_", num e texto, e chama a função camada do objeto game, passando os argumentos "drag" e 1500.

	A função random_mf recebe um parâmetro max e retorna um número inteiro aleatório entre 1 e o valor de max.

	A função log_key seleciona o elemento HTML com o ID "body" e armazena-o na variável log.

	A função log_down recebe uma função como parâmetro e adiciona um ouvinte de evento de tecla pressionada ao documento, que chama a função passada como parâmetro sempre que uma tecla é pressionada.

	A função log_up é semelhante à função log_down, mas adiciona um ouvinte de evento de tecla liberada ao documento.

	A função opacity recebe um ID de elemento HTML e um valor de opacidade como parâmetros. Ela seleciona o elemento com o ID especificado e define sua opacidade como o valor passado como parâmetro.

	A função type_curso recebe um ID de elemento HTML e um tipo de cursor como parâmetros. Ela seleciona o elemento com o ID especificado e define seu tipo de cursor como o valor passado como parâmetro.

	A função get_input recebe um ID de elemento HTML como parâmetro. Ela seleciona o elemento com o ID especificado, obtém o valor do seu campo de entrada e retorna esse valor.

	A função fixed_body recebe um valor de zoom como parâmetro e define o estilo de vários elementos HTML no corpo do documento para criar um efeito de tela fixa com o zoom especificado.

	A função camera recebe cinco parâmetros: o especto da câmera (2D ou canvas:2D), as coordenadas x e y da câmera, e os limites x e y da câmera. Se o especto for "2D" ou "2D", ela verifica se as coordenadas x e y estão dentro dos limites especificados e, se estiverem, move a janela do navegador para essas coordenadas. Se o especto for "canvas:2D" ou "canvas:2D", a função não faz nada. Caso contrário, ela exibe uma mensagem de erro no console.

	A função camera_move recebe um array de IDs de elementos HTML e uma quantidade de deslocamento x como parâmetros. Ela seleciona cada elemento com o ID especificado e define sua propried
	

	Descrição: fpsFrame(obj, func, fps) Uma função para limitar os frames por segundo de uma animação.
	Parâmetros:
	    obj: um objeto para acompanhar os frames por segundo
	    func: uma função de retorno para ser executada quando o limite de fps for atingido
	    fps: os frames por segundo desejados
	Valor de retorno: nenhum

	Descrição:  frame_sprite(name, src, context, width, height, frameIndex, row, tickCount, ticksPerFrame, frames) Uma função para criar um objeto sprite com propriedades de animação
		Parâmetros:
		    name: uma variável para armazenar o objeto sprite
		    src: a fonte de imagem do sprite
		    context: o contexto do canvas para renderizar o sprite
		    width: a largura de cada frame do sprite
		    height: a altura de cada frame do sprite
		    frameIndex: o índice do frame sprite atual
		    row: a linha do frame sprite atual
		    tickCount: a contagem de ticks desde a última mudança de frame
		    ticksPerFrame: o número de ticks antes de mudar para o próximo frame
		    frames: o número total de frames na folha de sprite
		Valor de retorno: o objeto sprite
	  update_sprite: Essa função é responsável por atualizar o sprite de uma imagem. Ela recebe como parâmetro o objeto que representa o sprite e atualiza o índice do quadro atual do sprite, de acordo com o número de ticks por quadro.

	render_sprite: Essa função é responsável por renderizar o sprite de uma imagem em um contexto. Ela recebe como parâmetros o objeto que representa o sprite, o contexto em que o sprite será desenhado e as coordenadas x e y onde o sprite será desenhado. Ela cria uma nova imagem, define as coordenadas de corte de acordo com o índice do quadro atual e desenha o sprite no contexto. Depois, chama a função update_sprite para atualizar o quadro atual.

	img_canvas: Essa função é responsável por desenhar uma imagem em um contexto de canvas. Ela recebe como parâmetros o contexto, um objeto que representa a imagem, a fonte da imagem, as coordenadas x e y onde a imagem será desenhada, a largura e altura da imagem e um parâmetro para indicar se a imagem está ativa ou não. Se a imagem estiver ativa, ela cria um novo objeto de imagem, define a fonte da imagem, e desenha a imagem no contexto.

	obj_in_obj: Essa função é responsável por adicionar um objeto filho a um objeto pai no HTML. Ela recebe como parâmetros o ID do objeto pai e o ID do objeto filho e adiciona o objeto filho como um elemento filho do objeto pai.

	remove_class: Essa função é responsável por remover uma classe CSS de um elemento HTML. Ela recebe como parâmetros o ID do elemento e o nome da classe a ser removida.

	get_window_w: Essa função retorna a largura da janela do navegador em pixels.

	get_window_h: Essa função retorna a altura da janela do navegador em pixels.

	responsive_img: Essa função é responsável por redimensionar uma imagem de acordo com as dimensões da janela do navegador. Ela recebe como parâmetro o ID da imagem e retorna um objeto com as novas dimensões da imagem.

	move_responsive: Essa função é responsável por mover um objeto na tela em uma posição específica, levando em consideração as dimensões da janela do navegador. Ela recebe como parâmetros o ID do objeto, a coordenada x e y da nova posição. 
	    animar_obj: Anima um objeto HTML usando CSS.
    text_bot: Cria um efeito de digitação em um elemento HTML.
   
    touchpad: Cria um touchpad virtual para dispositivos móveis.
   
    get_text: Obtém o texto de um elemento HTML e retorna como um número.
    
    set_text: Define o texto de um elemento HTML.
    
    edite_text: Edita o texto de um elemento HTML.
    
    modal: Cria um modal personalizado que pode ser exibido na tela.
    
    gravity: implementa a física de gravidade para um objeto em relação a outros objetos em seu ambiente
    
    force_gravity: implementa a força da gravidade em um objeto em relação a outros objetos em seu ambiente
    
    jump: implementa a mecânica de saltos para um objeto
    
    Rel_distanica: calcula a distância relativa entre dois objetos em movimento
    
    colidir_obj: verifica se dois objetos colidiram
    
    colidir_aq: verifica se um objeto está dentro de uma área específica
   
    right_check: verifica se um objeto está à direita de outro
   
    top_up_check: verifica se um objeto está acima de outro.
    
        colidir_force_r: essa função verifica se o objeto identificado pelo ID id1 colidiu com o objeto identificado pelo ID id2, com o lado direito do objeto id1 atingindo o lado esquerdo do objeto id2. O parâmetro check_contato é uma flag que indica se é para verificar se houve contato entre os objetos ou não. Se check_contato for true, a função verifica se os objetos estão em contato. Se check_contato for false, a função verifica se os objetos estão próximos o suficiente para colidir. A função retorna true se os objetos colidiram e false caso contrário.

    colidir_force_l: essa função é semelhante à função colidir_force_r, mas verifica se o lado esquerdo do objeto id1 colidiu com o lado direito do objeto id2.

    colidir_cal: essa função é usada pelas funções colidir_force_r e colidir_force_l para verificar se dois intervalos se sobrepõem. Ela recebe como parâmetros os valores mínimos e máximos dos dois intervalos e retorna true se os intervalos se sobrepõem e false caso contrário.

    colidir: essa função verifica se dois retângulos colidiram. Ela recebe como parâmetros dois objetos que contêm as coordenadas dos lados esquerdo, direito, superior e inferior do retângulo. A função utiliza a função colidir_cal para verificar se houve colisão nos eixos horizontal e vertical.

    coord: essa função retorna as coordenadas do retângulo identificado pelo ID passado como parâmetro. A função utiliza a função getBoundingClientRect para obter as coordenadas.

    rest: essa variável é uma referência à função requestAnimationFrame, que é utilizada para criar um loop de renderização do jogo.

    loop: essa variável é uma referência à função requestAnimationFrame, que é utilizada para criar um loop de renderização do jogo. É semelhante à variável rest.

    update: essa função é utilizada para atualizar o jogo em um intervalo de tempo determinado pelo parâmetro fps. A função recebe como parâmetros a função do jogo a ser atualizada e a taxa de quadros por segundo desejada. A função utiliza a função setInterval para atualizar o jogo a cada intervalo de tempo especificado em fps.
    

#Exemplo 1: Criar objeto com Classe Nandraki



	class Nandraki {
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
	}

	    Passo 1: Defina uma nova classe chamada Nandraki usando a palavra-chave class.
	    Passo 2: Dentro da classe, defina o método constructor com os parâmetros id,vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame.
	    Passo 3: Atribua esses parâmetros às propriedades correspondentes do objeto usando a sintaxe this.propriedade = valor.
	    Passo 4: Defina a propriedade body como o elemento HTML com o ID especificado por id usando document.getElementById.
	    Passo 5: O objeto Nandraki agora está pronto para ser instanciado usando a palavra-chave new.
	    
	    todos metodos da class Nandraki.js:
	    
	    Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)	
	    Nandraki. create_ui(id,txt,cor)
 	    Nandraki.move_obj(id,left,top,fixed)
            Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)	
            constructor(id,vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame)
            Nandraki. create_ui(id,txt,cor)
            Nandraki.move_obj(id,left,top,fixed)
