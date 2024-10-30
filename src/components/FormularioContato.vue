<template>
    <div class="areacontato">
        <div class="contato">
            <div class="formulario">
                <form method="get">
                    <h3 class="news">NEWSLETTER</h3>
                    <input type="text" placeholder="Nome:">
                    <input type="email" placeholder="Email:">
                    <textarea name="textarea" rows="10" cols="35" placeholder="Mensagem"></textarea> 
                    <a  class="club" href="#">JUNTE-SE AO CLUB</a>
                </form>
            </div>

            <div class="barmen"></div>

            <div class="contatos">
                <img class="icone" :src="logo">
                <h2 class="ctt">Contatos</h2>
                <h3 class="ctt1">Fone: (85) 91111-2222</h3>
                <h2 class="ctt">Email</h2>
                <h3 class="ctt1">bebidas@gmail.com</h3>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: "formularioContato",
        props: ["logo"],

        data(){
            return{

            }
        }
    }
</script>

<style>
    .areacontato{
        border: solid 2px white;
        height: 400px;
        display: flex;
        justify-content: center;
        background-color: white;
    }

    .contato{
        border: solid 0px blue;
        width: 1200px;
        display: flex;
        justify-content: space-evenly;
    }

    .barmen{
        border: solid 0px black;
        width: 400px;
        height: 398px;
        background-image: url('@/assets/garcon.jpg');
        background-size: cover;
        background-position: center;
    }

    .formulario, .contatos{
        border: solid 0px black;
        width: 300px;
        height: 396px;
    }

    .news{
        color: black;
    }

    form input{
        width: 282px;
        height: 35px;
        font-size: 15px;
        margin-bottom: 18px;
        border-radius: 4px;
        border: solid 2px rgb(204, 204, 204);
        background-color: rgb(233, 233, 233);
        color: black;
        padding-left: 10px;
        outline: none;
        margin-top: -10px;
    }

    textarea{
        width: 282px;
        font-size: 15px;
        border-radius: 4px;
        border: solid 2px rgb(204, 204, 204);
        background-color: rgb(233, 233, 233);
        margin-bottom: 18px;
        color: black;
        padding-left: 10px;
        outline: none;
    }

    .club{
        padding: 8px 82px;
        background-color: rgb(170, 139, 59);
        color: black;
        text-decoration: none;
    }

    .contatos{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .icone{
        width: 120px;
        border-radius: 20px;
    }

    .ctt{
        color: black;
    }

    .ctt1{
        position: relative;
        margin-top: -14px;
        color: black;
    }

</style>