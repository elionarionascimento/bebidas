<template>
    <div class="areainfo1">
        <div class="informacoes">
            <div class="grid1">

                <div class="historia">
                    <h4>Who are we and...</h4>
                    <h2>WHERE WE STAND FOR</h2>

                    <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                    Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                    when an unknown printer took a galley of type and scrambled it to make a type 
                    specimen book.</p>

                    <a href="#" class="historia_botao"> CONHEÇA NOSSA HISTÓRIA</a>
                </div>

            </div>

            <div class="grid2">
                    <div class="parte1">
                        <div class="pre">
                            <img class="cerveja" :src="cerveja">
                            <h4>PREMIUM BLENDED</h4>
                            <p>Clareza é um processo dinâmico que segue a mudança</p>
                        </div>

                        <div class="mat">
                            <img class="barril" :src="barril">
                            <h4>MATURED IN BARRELS</h4>
                            <p>Clareza é um processo dinâmico que segue a mudança</p>
                        </div>
                    </div>

                    <div class="parte2">
                        <div class="pre">
                            <img class="cerveja" :src="chope">
                            <h4>DISTILLED IN SCOTLAND</h4>
                            <p>Clareza é um processo dinâmico que segue a mudança</p>
                        </div>
                        <div class="mat">
                            <img class="barril" :src="qualidade">
                            <h4>COMMITMENT TO QUALITY</h4>
                            <p>Clareza é um processo dinâmico que segue a mudança</p>
                        </div>
                    </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: "InfoBebidas",
        props:["cerveja", "barril", "chope", "qualidade"],

        data(){
            return{
                
            }
        }
    }
</script>

<style>

    .grid2 .parte1, .parte2, .pre .mat{
        text-align: center;
    }

    .areainfo1{
        border: solid 0px white;
        height: 350px;
        display: flex;
        justify-content: center;
    }

    .informacoes{
        border: solid 0px orange;
        width: 1200px;
        height: 347px;
        display: flex;
        justify-content: center;
    }

    .grid1{
        border: solid 0px blue;
        width: 50%;
        background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('@/assets/barris.jpg');
        background-position: center;
        background-size: cover;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .grid2{
        border: solid 0px blue;
        width: 50%;
    }

    .parte1, .parte2{
        border: solid 0px greenyellow;
        height: 50%;
        display: flex;
    }

    .pre, .mat{
        border: solid 1px gray;
        width: 50%;
    }

    h4{
        color: rgb(170, 139, 59);
        margin-top: 12px;
    }

    .cerveja{
        width: 50px;
        margin-top: 20px
    }

    .barril{
        width: 35px;
        margin-top: 15px
    }

    .historia{
        border: solid 0px blue;
        width: 80%;
        height: 70%;
    }

    .historia h4{
        font-size: 20px;
    }

    .historia h2{
        position: relative;
        margin-top: -22px;
        font-size: 28px;
    }

    .historia p{
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        margin-bottom: 40px;
    }

    .historia_botao{
        padding: 10px 15px;
        background-color: white;
        border: solid 2px black;
        color: black;
        text-decoration: none;
        font-size: 13px;
    }
</style>