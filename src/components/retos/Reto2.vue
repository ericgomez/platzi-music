<template lang="pug">
  #App
    section.header
      .logo
        img(src="https://static.platzi.com/media/user_upload/logo-d871d30b-ac23-4240-93f3-13e49084d80b.jpg" alt="")
      .buscar
        input.buscar_texto(type="text" placeholder="Busca tu película, actor, o director favorito.")
      .usuario
        h2.usuario_text Kiyosaki
        img.avatar(src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTyv-9ZkEOJqXyELYYJZ3UJ_bvqVhIkaYGL0cpVIVrZr5v-fF7c7O2UZP6W_ISSeIE5rxUZPPMiy7nPNXhYjPwh6hM9Dsse_yBq1w&usqp=CAU&ec=45761792" alt="")
        icon.opciones
          i(class="fas fa-fire fa-2x")
    section.menu_lateral
      .menu_container_top
        .opcion_menu
          icon.icono
            i(class="fas fa-home fa-2x")
          label Home
        .opcion_menu
          icon.icono
            i(class="fas fa-fire fa-2x")
          label Trending
        .opcion_menu
          icon.icono
            i(class="fas fa-heart fa-2x")
          label Más likes
      .menu_container_bottom
        .opcion_menu
          icon.icono
            i(class="fas fa-cog fa-2x")
          label Ajustes

    section.main
      h2.texto_categoria Ahora en el cine
      .pelicula_categoria
        .pelicula
          img.foto_pelicula(src="https://i1.wp.com/www.sopitas.com/wp-content/uploads/2019/05/up-pelicula-quiz.jpg" alt="")
          .pelicula_hover
            h2 Up
            p.descripcion_pelicula Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, praesentium
        .pelicula
          img.foto_pelicula(src="https://i.blogs.es/554926/carlyesposa/450_1000.jpg" alt="")
          .pelicula_hover
            h2 Up
            p.descripcion_pelicula Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, praesentium
        .pelicula
          img.foto_pelicula(src="https://blog.stannah.co/wp-content/uploads/sites/17/2019/10/carl-russel-dug.jpg" alt="")
          .pelicula_hover
            h2 Up
            p.descripcion_pelicula Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, praesentium
      h2.texto_categoria Ahora en el cine
      .pelicula_categoria
        .pelicula
          img.foto_pelicula(src="https://fotografias.flooxernow.com/clipping/cmsimages01/2020/01/09/44992B47-09FA-4EE9-9B24-E9100A76CB2F/58.jpg" alt="")
          .pelicula_hover
            h2 Up
            p.descripcion_pelicula Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, praesentium
        .pelicula
          img.foto_pelicula(src="https://blog.stannah.co/wp-content/uploads/sites/17/2019/10/russell-carl.jpg" alt="")
          .pelicula_hover
            h2 Up
            p.descripcion_pelicula Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, praesentium
        .pelicula
          img.foto_pelicula(src="https://www.tuenlinea.com/wp-content/uploads/2018/08/Abuelitos-festejan-su-60-Aniversario-llevando-a-la-realidad-la-peli-UP-1280x720.jpg" alt="")
          .pelicula_hover
            h2 Up
            p.descripcion_pelicula Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, praesentium

</template>

<script>

export default {
  name: 'Reto2',
  components: {
  //  HelloWorld
  }
}
</script>

<style>
 @import'//use.fontawesome.com/releases/v5.0.7/css/all.css';
 @import'https://fonts.gstatic.com';
 @import'https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700&display=swap';

#App {
  font-family: 'Lato', sans-serif;
  width: 1024px;
  margin: 0 auto;

}

/* header */
.header{
  display: flex;
  height: 72px;
  align-items: center;
   box-shadow: 0px0px3px3px#ccc
}

.logo{
  width:200px;
}

.buscar{
  width:600px;
  text-align: center;
  margin-top: 6px;
  margin-left: 32px;
}

.buscar_texto{
  display: block;
  width: 100%;
  padding: 2px6px;
  font-size: 16px;
  line-height: 24px;
}

.usuario{
  width: 224px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
}

.usuario_text{
  margin-right: 8px;
  font-size: 16px;
  color: #38292a;
}
.avatar{
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 8px;
}

.usuario.opciones{
  margin-right: 16px;
}

/* Menu Laterial */
.menu_lateral{
  float: left;
  width: 89px;
  height: 810px;
  background: linear-gradient(to right,  #FF535B, #FD746C);
  text-align: center;
}
.menu_container_bottom{
  margin-top: 330px;
  padding-top: 16px;
  height: 60px;
}
.opcion_menuicon, .opcion_menulabel{
  color: white;
  display: block;
  margin-top: 16px;
}

/* Main */
.main{
  float: left;
  width: 935px;
}

.texto_categoria{
  margin-left: 16px;
  font-size: 20px;
}

.pelicula_categoria{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
}

.pelicula{
  width: 287px;
  height: 192px;
  margin-bottom: 10px;
  position: relative;
  cursor: pointer;
  color: #ffffff;
}
img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
}

.pelicula_hover{
  position: absolute;
  padding: 8px;
  width: 271px;
  height: 84px;
  top: 92px;
  background: rgba(255, 83, 91, 0.7);

}
.pelicula_hoverh2, .pelicula_hoverp{
  margin: 0px;
}

</style>
