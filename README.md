Welcome to the Nandraki.js!

    |
    2.0 .0 >= function game.canvas_start("canvas", 800, 500) && game.context("canvas")

    |
    Beta version 2023[3.0]



Verficar Version

Nandraki.version();

Parametros basico
id = string do document.getElementById(id) ex: "player" = < div id = "player" > < /div>

    obj = elemento game.get_obj(id)

get_obj: function(id) {
        let element = document.getElementById(id);
        return element;

    },

    Criar obj com Class Nandraki
constructor(id, vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame) {
    obj.id = id;
    obj.vida = vida;
    obj.gravidade = gravidade;
    obj.velocidade = velocidade;
    obj.massa = massa;
    obj.di = di;
    obj.up = up;
    obj.mirror = mirror;
    obj.anim = anim;
    obj.jump = jump;
    obj.frame = frame;
    obj.body = document.getElementById(obj.id);

}
Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)
Nandraki.create_ui(id, txt, cor)
Nandraki.move_obj(id, left, top, fixed)


Detectar colisão Nandraki.js


if (game.check_colidir("box_chao", "box_player") == true && game.check_id("box_chao") == true) {

    //player.up=player.up
    //player.di=player.di
    //return true

}


Start game

//javascript e html{

game.create_obj(div, text);

myjogo = {


    loop: function() {


        Nandraki.create_ui("text", " Hello world!", "ffff");


    },
}

fps = 60;
game.update(myjogo.loop, fps);

// }

//canvas game{  

function game() {

    Nandraki.clearRect(0, 0, canvas.width, canvas.height);
    Nandraki.beginPath();

    Nandraki.stroke();
    game.rest(game, canvas);
}
game.loop(game, canvas)

//}

Criar canvas

game.canvas_start(id, width, height);

Canvas Text

game.canvas_text(text, font, cor, x, y);

Canvas Arc

game.canvas_arc(x, y, font, b, p);


Game Print

game.print("ola mundo");


force_obj
function(id, x, y, rotate)

//  rotate true = translate3d("+x+"px,"+y+"px, 0px) rotateY(180deg)	
//   rotate false = translate3d("+x+"px,"+y+"px, -0px) rotateY(0deg)

game.force_obj(item1.id, item1.di, item1.gravidade, true)

//ir para frente dentro do loop
item1.di++
game.force_obj(item1.id, item1.di, item1.gravidade, true)


Simples gravidade div dom

game.force_obj("id", x, y, false)
y += gravitySpeed;
var end = 500;
if (y >= end) {
    y = end;
    gravitySpeed = 5
    pulo = 1
    //gravitySpeed = -(gravitySpeed * bounce);

} else {

    gravitySpeed += gravity;

}
or

obj = {
    up: 0,
    di: 0,
    velocidade: 0,
    gravidade: 0.05

}

game.force_obj("id", x, obj.up, false)
game.gravity(obj, fim, bounce, velue)

Click Mouse

function click() {

    game.print("click");
}
game.click_start("id do obj", click);


Move Mouse

game.move_mouse(id do obj);



create box

game.create_box(id, debug);


Touch start e and


function click() {

    game.print("touch start ative");

}
game.touch_end("id do obj", click);
// or 
game.touch_start("id do obj", click);


Add obj dentro de outro obj

game.obj_in_obj(id do obj1, id do obj2);

Set Text

game.set_text(id do obj, "texto");
game.set_text(id do obj, 1 + 1);

Teclado log keydown keyup

game.log_key;
game.log_down(logKey1);

function logKey1(e) {
    if (e.code == "KeyS") {
        game.print("Test log key down ok!");
    }
}
game.log_up(logKey2);

function logKey2(e) {
    if (e.code == "KeyS") {
        game.print("Test log key up ok!");
    }
}


Scale X

game.scaleX("id player ou obj", "-1");

Random Math

random_m(max, min, variante);

Random Math floor

random_mf(max, min, variante);

Opacity

opacity(id, value);


kill_free

//deletar obj=html
kill_free(id);




som_play

game.som_play(id, path som);



touchpad virtual

html in body {
    <
    div id = "joy" >
        <
        /div>
}
game.touchpad("joy", set left, set top);
stick = game.get_obj("stick");
base = game.get_obj("base-stick");

if (stick.offsetLeft == 32) {
    Player.anim = "parado";
    Player.di = Player.di;
}

if (stick.offsetLeft < 32) {
    Player.di -= 2
    Player.anim = "correndo_lateral2"
} else if (stick.offsetLeft > 32) {
    Player.di += 2
    Player.anim = "correndo_lateral1"
}
if (stick.offsetTop <= -1) {
    Player.up -= 2
    Player.anim = "correndo_up"

}
if (stick.offsetTop == 32) {
    Player.anim = "parado";
    Player.di = Player.di;

}
if (stick.offsetTop > 32) {
    Player.up += 2
    Player.anim = "correndo_down"

}


Create sprite

//create_sprite(id,camadas,img1,img2,img3,img4,img5,width,height,boxl,boxh,left,top)

//cada img gera um id "img[nivel da camada]player"  

//boxl=x boxh=y são coodernada do box collider 2d do objeto.Ative sempre o Nandraki.create_box("box_player",true);

//todo sprite tem seu box_id

Nandraki.create_sprite("vida", 1, "item.png", null, null, null, null, 16, 16, 9, 14, 28, 25);


img frame

//img_frame: function(id,id da img = por padrão sempre vai ser img[3]+id do obj ,width,height,calculo do frame,inicio do frame,frame variavel,reset frame)
//img_id sempre vai ter padrão de img[3]id. 
//[3] = camanda da imgame 3 do objeto

if (player.anim == "run") {

    game.img_frame(id, "img[3]player", 64, 32, 7, player.frame++, 7, 0);
    if (frame == 7) frame = 0

}

bd_save: function(variavel, value)

localStorage.setItem(variavel, value);



bd_load: function(variavel)

game.bd_load(variavel)


bd_remove: function(variavel)

game.bd_remove(variavel)


bd_clear: function()

game.bd_clear();


Camera: function()

game.camera("2d", x, y, limitX, limitY)

spawn sprite: function()

game.spawn_sprite(id, img, left, top);

display item: function()

// none=ocuto
// block=visivel
game.display(id obj, "none")

start canvas: function()

game.canvas_start("canvas", 800, 500)
game.context("canvas") //return context Nandraki

//in loop game{
Nandraki.functionCanvas

Nandraki.clearRect(0, 0, canvas.width, canvas.height);
Nandraki.beginPath();
Nandraki.stroke();
//}

context: function(id)

//canvas = document.getElementById(id);
//Nandraki = canvas.getContext('2d');

game.context("canvas id") //return Nandraki;

loop canvas:

    function game() {

        Nandraki.clearRect(0, 0, canvas.width, canvas.height);
        Nandraki.beginPath();

        Nandraki.stroke();
        game.rest(game, canvas);
    }
game.loop(game, canvas)

canvas_rect: function()

game.canvas_rect(Nandraki, 0, 430, 500, 50)


img_canvas: function(context, obj, src, x, y, width, height, ative) return obj {
    x: x,
    y: y,
    ative: true or false
}

bloco = game.img_canvas(Nandraki, "bloco", "bloco.png", 10, 10, 64, 64, true)
//bloco.x return 10
//bloco.y return 10
//bloco.ative return true

frame_sprite: function(name, src, context, width, height, frameIndex, row, tickCount, ticksPerFrame, frames) return name

//context canvas Nandraki

runPlayer = game.frame_sprite("player", "player.png", Nandraki, 64, 64, 0, 5, 0, 5, 5)


render_sprite: function(obj, context, x, y)

//context canvas Nandraki

game.render_sprite(runPlayer, Nandraki, x, y)

gravity: function(obj, target_id = [], force_jump = 5, bonce_bool = false, bounce_value = 0.8)

obj = {
    up: 0,
    dir: 0,
    velocidade: 0,
    gravitySpeed: 0,
    gravidade: 0.05,
    id: "bloco"
}

game.gravity(obj, ["fundo", "item", "item1"], 3, false, 1.5)

jump: function(obj = {
    up: 0,
    velocidade: 0.50,
    gravitySpeed: 0.5
}, force = 25, gravidade = 1)

game.jump(obj, 25, 0.8);

force_gravity: function(obj, target_arry = [])

game.force_gravity(obj, ["item1", "item2", "item3"])

gravity_targetM: function(obj, target = 100, bounce = false or true, force = 5)

obj = {
    up: 0,
    dir: 0,
    velocidade: 0,
    gravitySpeed: 0,
    gravidade: 0.05,
    id: "bloco"
}
game.gravity_targetM(obj, 150, false, 5)

gravity_targetF: function(obj, target = 100, bounce = false or true, force = 5, func)
obj = {
    up: 0,
    dir: 0,
    velocidade: 0,
    gravitySpeed: 0,
    gravidade: 0.05,
    id: "bloco"
}

function start_func() {
    console.log("ative!")
}
game.gravity_targetF(obj, target, false, start_func)

get[x] / [y] in game: function arg(id)

game.get_left(id) - >
    return document.getElementById(id).offsetLeft;
game.get_top(id) - >
    return document.getElementById(id).offsetTop;

translate3d(tx, ty, tz) {
    [element.style.transform = "translate3d(" + x + "px," + y + "px, 0px)";]
    [requerimento: game.force_obj(id, x, y, true or false)]

    game.get_tx(id) - >
        return matrix.m41 traform3dX
    game.get_ty(id) - >
        return matrix.m42 traform3dY

}
camera_move: function(id = [], x)

x += 10
game.camera_move(["fundo", "item", "item1"], x)

obj_in_obj: function(obj, id)

document.getElementById(obj).appendChild(document.getElementById(id));

remove_class: function(id, obj)

let element = document.getElementById(id);
element.classList.remove(obj);

get_window_w: function()

return window.innerWidth;
user
function = game.get_window_w()

get_window_h: function() {

        return window.innerHeight;

        user
        function = game.get_window_h()

        responsive_img: function(id)

        return game.img_size(id, game.get_window_w(), game.get_window_h())

        user
        function = game.responsive_img("fundo")

        move_responsive(id, x, y)

        Nandraki.move_obj(id, game.get_window_w() / 2 / 5 + x, game.get_window_h() / 2 + y, true)
        user
        function = game.move_responsive("fundo")

        objH: function(id)

        return parseInt(game.get_obj(id).style.height)
        user
        function = x = game.objH("fundo")

        objW: function(id)

        return parseInt(game.get_obj(id).style.width)
        user
        function = x = game.objW("fundo")

        move_parent: function(id1, id2)

        let div_p = document.getElementById(id1);
        let obj = document.getElementById(id2);
        div_p.appendChild(obj.parentElement);
        user
        function = game.move_parent("player", "item")
