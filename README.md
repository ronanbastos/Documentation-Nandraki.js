converte esse texto em html: Welcome to the Nandraki.js!

|2.0.0>= function game.canvas_start("canvas",800,500) && game.context("canvas")

|Beta version 2023 [3.0]

Nandraki.version();

Criar obj com Class Nandraki

Parametros basico id = string do document.getElementById(id) ex:"player" =

obj = elemento game.get_obj(id)

get_obj: function (id) {
	let element = document.getElementById(id);
	return element;

},

Criar obj com Class Nandraki constructor(id,vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame){ obj.id = id; obj.vida = vida; obj.gravidade = gravidade; obj.velocidade = velocidade; obj.massa = massa; obj.di = di; obj.up = up; obj.mirror = mirror; obj.anim = anim; obj.jump = jump; obj.frame = frame; obj.body = document.getElementById(obj.id);

     }
     Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)	
     Nandraki. create_ui(id,txt,cor)
     Nandraki.move_obj(id,left,top,fixed)
        //Nandraki.create_sprite(id, camadas, img1, img2, img3, img4, img5, width, height, boxl, boxh, left, top)	
       //constructor(id,vida, gravidade, velocidade, massa, di, up, mirror, anim, jump, frame)
      //Nandraki. create_ui(id,txt,cor)
     //Nandraki.move_obj(id,left,top,fixed)

Detectar colisão Nandraki.js

	game.move_mouse(id do obj);

Move Mouse

	game.move_mouse(id do obj);

create box

kill_free

  kill_free(id);

//deletar obj=html
  kill_free(id);

som_play

//context canvas Nandraki

game.render_sprite(runPlayer,Nandraki,x,y)	

gravity: function (obj, target_id = [], force_jump = 5, bonce_bool = false, bounce_value = 0.8)

obj={
	up:0,
	dir:0,
	velocidade:0,
	gravitySpeed:0,
	gravidade:0.05,
	id:"bloco"
}

game.gravity(obj,["fundo","item","item1"],3,false,1.5)	

jump: function (obj = { up: 0, velocidade: 0.50,gravitySpeed:0.5 },force=25,gravidade=1)

game.jump(obj,25,0.8);

force_gravity:function(obj, target_arry = [])

 game.force_gravity(obj,["item1","item2","item3"])

gravitygravity_targetM: function (obj, endtarget=100, bounce, velue=false or true,force=5)

obj={
	up:0,
	dir:0,
	velocidade:0,
	gravitySpeed:0,
	gravidade:0.05,
	id:"bloco"
up:0,
velocidade:0,
gravidade:0.05
}
game.gravity_targetM(obj,150,false,5)	

game.gravity(obj,500,false,0.5)

gravity_targetF: function (obj, target=100, bounce=false or true,force=5,func) obj={ up:0, dir:0, velocidade:0, gravitySpeed:0, gravidade:0.05, id:"bloco" } function start_func(){ console.log("ative!") } game.gravity_targetF(obj, target,false, start_func)

get [x]/[y] in game: function arg (id)

  game.get_left(id) -> return document.getElementById(id).offsetLeft;
  game.get_top(id) -> return document.getElementById(id).offsetTop; 
  
  translate3d(tx, ty, tz){
  	  [element.style.transform = "translate3d(" + x + "px," + y + "px, 0px)";]	
	  [requerimento:game.force_obj(id,x,y,true or false)]
	  
	  game.get_tx(id) -> return matrix.m41 traform3dX 
	  game.get_ty(id) -> return matrix.m42 traform3dY 
	  
   }

camera_move: function (id=[], x)

	x+=10
	game.camera_move(["fundo","item","item1"],x)

obj_in_obj: function (obj, id)

    document.getElementById(obj).appendChild(document.getElementById(id));

remove_class: function (id, obj)

    let element = document.getElementById(id);
    element.classList.remove(obj);

get_window_w: function ()

    return window.innerWidth;
user function = game.get_window_w()

get_window_h: function () {

    return window.innerHeight;

user function = game.get_window_h()

responsive_img: function (id)

    return game.img_size(id, game.get_window_w(), game.get_window_h())

user function = game.responsive_img("fundo")

move_responsive(id, x, y)

    Nandraki.move_obj(id, game.get_window_w() / 2 / 5 + x, game.get_window_h() / 2 + y, true)
user function = game.move_responsive("fundo")

objH: function (id)

    return parseInt(game.get_obj(id).style.height) 
user function = x=game.objH("fundo")

objW: function (id)

    return parseInt(game.get_obj(id).style.width)
user function = x=game.objW("fundo")

move_parent: function (id1,id2)

    let div_p = document.getElementById(id1);
    let obj = document.getElementById(id2);
    div_p.appendChild(obj.parentElement);
user function = game.move_parent("player","item")
