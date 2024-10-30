<template>
    <div class="areafundo"> 
        <div class="fundo">
            <div class="lista1">
                <h3>ÚTIL</h3>
                <a href="#"> <p>Home</p> </a>
                <a href="#"> <p>Distruidores</p> </a>
                <a href="#"> <p>Blog</p> </a>
                <a href="#"> <p>Login</p> </a>
            </div>

            <div class="lista2">
                <h3>Ajuda</h3>
                <a href="#"><p>Serviços</p></a>
                <a href="#"><p>Descubra</p></a>
                <a href="#"><p>Pedidos Recentes</p></a>
                <a href="#"><p>Contatos</p></a>
                <a href="#"><p>termos & privacidades</p></a>
            </div>

            <div class="lista3">
                <h3>ÚTIL</h3>
                <a href="#"><p>Lorem ipsum</p></a>
                <a href="#"><p>Lorem ipsum</p></a>
                <a href="#"><p>Lorem ipsum</p></a>
                <a href="#"><p>Lorem ipsum</p></a>
                <a href="#"><p>Lorem ipsum</p></a>
            </div>

            <div class="lista4">
                <div class="infor1">
                    <img class="local" :src="local">
                    <p>Area 51, USA</p>
                </div>

                <div class="infor1">
                    <img class="local" :src="carta">
                    <p>infodrinks@gmail.com</p>
                </div>

                <div class="infor1">
                    <img class="local" :src="fone">
                    <p>(85) 91111-2222</p>
                </div>
            </div>

            <div class="lista5">
                <div>
                    <img class="lg_fundo" :src="logo_fundo">
                </div>

                <div class="sociais">
                    <img class="icones" :src="insta">
                    <img class="icones" :src="face">
                    <img class="icones" :src="x">
                </div>
            </div>
        </div>
    </div>

    <hr class="linha">
</template>

<script>
    export default{
        name: "CapaFundo",
        props: ["local", "carta", "fone", "logo_fundo", "insta", "face", "x"],

        data(){
            return{

            }
        }
    }
</script>

<style>
    .areafundo{
        border: solid 0px blue;
        height: 300px;
        background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('@/assets/fundo.jpg');
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: center;
    }

    .fundo{
        border: solid 0px white;
        width: 1200px;
        height: 298px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .infor1{
        display: flex;
        align-items: center;
    }

    .local{
        width: 30px;
        height: 30px;
    }

    .lista1, .lista2, .lista3, a{
        text-decoration: none;
    }

    .lg_fundo{
        width: 150px;
        border-radius: 20px
    }

    .lista5{
        border: solid 0px orange;
        width: 250px;
        height: 150px;
        display: flex;
        justify-content: space-between;
    }

    .sociais{
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }

    .icones{
        width: 30px;
    }

    .linha{
        position: relative;
        margin-top: -10px;
        width: 1200px
    }
</style>