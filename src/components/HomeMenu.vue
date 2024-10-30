<template>
  <div class="areamenu">
    <div class="menus">
        <ul>
          <li><a href="#">HOME</a></li>
          <li><a href="#">HISTÓRIA</a></li>
          <li><a @mouseenter="abrirSubmenu" v-on:mouseleave="fecharSubmenu" href="#">BEBIDAS</a></li>
          
          <li>
            <a href="#">
                <img class="logo" :src="logo">
            </a>
          </li>
          
          <li><a @mouseenter="abrirSubmenuD" v-on:mouseleave="fecharSubmenuD" href="#">DRINKS</a></li>
          <li><a @mouseenter="abrirSubmenuC" v-on:mouseleave="fecharSubmenuC" href="#">VEM PRO CLUB</a></li>
          <li><a href="#">CONTATOS</a></li>
        </ul>
    </div>
  </div>

    <div class="areainfo">
        <div class="info">
            <div class="tiposbebidas0">
              
            </div>
            
            <div class="tiposdrinks0">
              
            </div>

            <div v-if="submenuAberto" class="submenu" @mouseout="fecharSubmenu">
              <ul>
                <li><a href="#">Absinto</a></li>
                <li><a href="#">cachaça</a></li>
                <li><a href="#">Gin</a></li>
                <li><a href="#">Rum</a></li>
                <li><a href="#">Whisky</a></li>
                <li><a href="#">Vodka</a></li>
                <li><a href="#">Cerveja</a></li>
                <li><a href="#">Vinho</a></li>
                <li><a href="#">Champanhe</a></li>
                <li><a href="#">Conheque</a></li>
              </ul>
            </div>

            <div class="tiposbebidas0">
              
            </div>
            
            <div v-if="mostrardrinks" class="tiposdrinks1" @mouseout="fecharSubmenuD">
              <ul>
                <li class="link"><a href="#">Aperol spritz</a></li>
                <li class="link"><a href="#">Moscow mule</a></li>
                <li class="link"><a href="#">Piña colada</a></li>
                <li class="link"><a href="#">Caipirinha</a></li>
                <li><a href="#">Cosmopolitan</a></li>
                <li><a href="#">Dry martini</a></li>
                <li><a href="#">Sex on the beach</a></li>
                <li><a href="#">Manhattan</a></li>
                <li><a href="#">Cuba libre</a></li>
                <li><a href="#">Daiquiri</a></li>
                <li><a href="#">Lagoa Azul</a></li>
                <li><a href="#">Soda italiana</a></li>
                <li><a href="#">White Russian</a></li>
              </ul>
            </div>

            <div v-if="mostrarclub" class="tiposclub1" @mouseleave="fecharAoSairDoConteudo">
              <ul>
                <li><a href="#">Pontos</a></li>
                <li><a href="#">Farras</a></li>
                <li><a href="#">Viagens</a></li>                
                <li><a href="#">Bares</a></li>                
                <li><a href="#">Restaurantes</a></li>             
              </ul>
            </div>

            <div class="tiposcontato">
              
            </div>
        </div>      
    </div>
</template>

<script>
export default{
  name: 'HomeMenu',
  props:["logo"],

  data(){
    return{
      submenuAberto: false,
      mostrardrinks: false,
      mostrarclub: false
    }
  },

  methods:{
    abrirSubmenu(){
      this.submenuAberto = true
    },

    fecharSubmenu(event){
      const menu = event.currentTarget;
      const rect = menu.getBoundingClientRect();
      const mouseX = event.clientX;
      const mouseY = event.clientY;

      const saiuForaB = mouseY < rect.top || mouseX < rect.left || mouseX > rect.right;

        if(saiuForaB){
          this.submenuAberto = false
        }
    },

    manterAberto(){
      this.mostrarbebidas = true
    },
/*----------------------------------------------------*/
    abrirSubmenuD(){
      this.mostrardrinks = true
    },

    fecharSubmenuD(event){
      const menuD = event.currentTarget;
      const rectD = menuD.getBoundingClientRect();
      const mouseXD = event.clientX;
      const mouseYD = event.clientY;

      const saiuForaD = mouseYD < rectD.top || mouseXD < rectD.left || mouseXD > rectD.right;

        if(saiuForaD){
          this.mostrardrinks = false
        }
    },

    manterAbertoD(){
      this.mostrardrinks = true
    },
/*---------------------------------------------------------*/
    abrirSubmenuC(){
      this.mostrarclub = true
    },

    fecharSubmenuC(event){
      const menuC = event.currentTarget;
      const rectC = menuC.getBoundingClientRect();
      const mouseXC = event.clientX;
      const mouseYC = event.clientY;

      const saiuFora = mouseYC < rectC.top || mouseXC < rectC.left || mouseXC > rectC.right;

        if(saiuFora){
          this.mostrarclub = false
        }
    },

    manterAbertoC(){
      this.mostrarclub = true
    },

    fecharAoSairDoConteudo(){
      this.mostrarclub = false
    }

  }
}
</script>

<style>

  .link{
    cursor: pointer;
  }

  .tiposbebidas0, .tiposdrinks0{
    border: solid 0px red;
    width: 200px
  }

  .tiposbebidas, .tiposdrinks, .tiposclub{
    border: solid 2px orange;
    width: 300px;
    height: 400px;
  }
  
  .submenu{
    border: solid 2px rgb(80, 79, 79);
    background-color: black;
    width: 278px;
    height: 410px;
    margin-left: -535px;
    display: flex;
    position: relative;
    z-index: 10;
  }

  .submenu ul{
    margin-top: 0px;
  }

  .tiposdrinks1{
    position: absolute;
    z-index: 10;
    border: solid 2px rgb(80, 79, 79);
    background-color: black;
    width: 278px;
    height: 534px;
    margin-left: -135px;
    display: flex;
    position: relative;
  }

  .tiposdrinks1 ul{
    margin-top: 0px;
  }

  .tiposclub1{
    position: absolute;
    z-index: 10;
    border: solid 2px rgb(80, 79, 79);
    background-color: black;
    width: 278px;
    height: 206px;
    margin-left: 250px;
    display: flex;
    position: relative;
  }

  .tiposclub1 ul{
    margin-top: 0px;
  }

  .submenu ul li{
    list-style: none;
    border-left: solid 0px white;
    border-right: solid 0px white;
    border-top: solid 0px gray;
    border-bottom: solid 2px gray;
    width: 278px;
    height: 40px;
    margin-left: -40px;
    display: flex;
    justify-content: center;
    align-items: center
    }

    .submenu ul li:hover{
      background-color: rgb(170, 139, 59)
    }
    
    
  .tiposbebidas1 ul li a{
    text-decoration: none;
  }

  .tiposdrinks1 ul li{
    list-style: none;
    border-left: solid 0px white;
    border-right: solid 0px white;
    border-top: solid 0px gray;
    border-bottom: solid 2px gray;
    width: 278px;
    height: 40px;
    margin-left: -40px;
    display: flex;
    justify-content: center;
    align-items: center
    }

    .tiposdrinks1 ul li:hover{
      background-color: rgb(170, 139, 59)
    }
    
    
  .tiposdrinks1 ul li a{
    text-decoration: none;
  }

  .tiposclub1 ul li{
    list-style: none;
    border-left: solid 0px white;
    border-right: solid 0px white;
    border-top: solid 0px gray;
    border-bottom: solid 2px gray;
    width: 278px;
    height: 40px;
    margin-left: -40px;
    display: flex;
    justify-content: center;
    align-items: center
    }

    .tiposclub1 ul li:hover{
      background-color: rgb(170, 139, 59)
    }
    
    
  .tiposclub1 ul li a{
    text-decoration: none;
  }

  .tiposcontato{
    border: solid 0px orange;
    width: 1cqmin;
    height: 400px;
    margin-left: 80px;
  }

  .info{
    border: solid 0px blue;
    width: 1200px;
    display: flex;
    justify-content: center;
    position: relative;
  }

  .areainfo{
    border: solid 0px white;
    height: 100px;
    display: flex;
    justify-content: center;
    position: relative;
  }

  .logo{
    width: 120px;
    border-radius: 20px;
    position: relative;
    margin-top: -10px;
  }

  .menus{
    border: solid 0px blue;
    width: 1200px;
  }

  .menus ul{
    display: flex;
    list-style: none;
    justify-content: space-between;
    margin-top: 30px;
  }

  .menus ul li{
    border: solid 0px white;
  }

  .menus ul li a{
    text-decoration: none;
  }
  
  .areamenu{
    border-top: solid 2px black;
    border-left: solid 2px black;
    border-right: solid 2px black;
    border-bottom: solid 3px rgb(170, 139, 59);
    height: 80px;
    background-color: black;
    display: flex;
    justify-content: center;
  }

  *{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  }
</style>
