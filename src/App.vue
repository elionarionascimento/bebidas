<template>
  <HomeMenu :logo="icone"/>
  <DestaqueBebidas :l1="primeiro" :l2="segundo" 
  :lb2="bombay1" :lb22="bombay2" :lb33="tanqueray" :lb4="chivas"></DestaqueBebidas>
  <Infobebidas :cerveja="simbolo1" :barril="simbolo2" 
  :chope="simbolo3" :qualidade="simbolo4"></Infobebidas>
  <ReceitasDrinks :receitalimao1="primeirareceita" :receitavermelho="drinkvermelho"
  :receitaroxo="terceirareceita" :drinkquatro="quartodrink"></ReceitasDrinks>
  <PaginaPremium :civas="civas1" :jack="jack2" :johny="johny3"></PaginaPremium>
  <FormularioContato :logo="icone"></FormularioContato>
  <MarcasBebidas :logo1="lg1" :logo2="lg2" :logo3="lg3"></MarcasBebidas>
  <CapaFundo :local="icone_local" :carta="icone_carta" 
  :fone="icone_fone" :logo_fundo="fundo_logo" :insta="icone_insta"
  :face="icone_face" :x="icone_x"></CapaFundo>
</template>

<script>
import HomeMenu from './components/HomeMenu.vue';
import DestaqueBebidas from './components/DestaqueBebidas.vue';
import Infobebidas from './components/Infobebidas.vue';
import ReceitasDrinks from './components/ReceitasDrinks.vue';
import PaginaPremium from './components/PaginaPremium.vue';
import FormularioContato from './components/FormularioContato.vue';
import MarcasBebidas from './components/MarcasBebidas.vue';
import CapaFundo from './components/CapaFundo.vue';
export default {
  name: 'App',
  components: {
    HomeMenu,
    DestaqueBebidas,
    Infobebidas,
    ReceitasDrinks,
    PaginaPremium,
    FormularioContato,
    MarcasBebidas,
    CapaFundo
  },

  data(){
    return{
      icone: './img/logob.jpg',
      primeiro: './img/l2.png',
      segundo: './img/l3.png',
      bombay1: './img/b1.png',
      bombay2: './img/b2.png',
      tanqueray: 'img/b3.png',
      chivas: 'img/c1.png',
      simbolo1: 'img/simbolo1.png',
      simbolo2: 'img/barril.png',
      simbolo3: 'img/simbolo3.png',
      simbolo4: 'img/qualidade.png',
      primeirareceita: 'img/drinklimao.png',
      drinkvermelho: 'img/drinkvermelho.png',
      terceirareceita: 'img/drinkroxo.png',
      quartodrink: 'img/drinkquatro.png',
      civas1: 'img/chivas1.png',
      jack2: 'img/jack2.png',
      johny3: 'img/walker3.png',
      lg1: 'img/logo1.png',
      lg2: 'img/logo2.png',
      lg3: 'img/logo3.png',
      icone_local: 'img/local.png',
      icone_carta: 'img/carta.png',
      icone_fone: 'img/telefone.png',
      fundo_logo: 'img/logob.jpg',
      icone_insta: 'img/insta.png',
      icone_face: 'img/face.png',
      icone_x: 'img/x.png',

    }
  }
}
</script>

<style>
body{
  background-color: rgb(26, 26, 26);
  margin: 0;
}

*{
  color: white;
}
</style>
