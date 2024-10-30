<template>
    <div class="areadrink">
        <div @click="mover02" class="botaod"><p>&lt;</p></div>
            <div class="destaquedrink">
                   <div class="destaque2" :style="{marginLeft: marginLeftDrink2 + 'px'}">
                        <div class="drink1">
                            <div class="receitas1">
                                <img class="receitalimao1" :src="receitalimao1"> 
                            </div>

                            <div class="receitainfo1">
                                <h4>Perfeito servido com</h4>
                                <h2 class="descricaodrink">LIMÃO E BOURBON</h2>

                                <p class="descricaodrink">Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                                Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                                when an unknown printer took a galley of type and scrambled it to make a type 
                                specimen book.</p>

                                <a href="#" class="drink_botao"> CONHEÇA NOSSA HISTÓRIA</a>
                            </div>
                        </div>

                        <div class="drink1">
                            <div class="receitas1">
                                <img class="receitavermelho" :src="receitavermelho"> 
                            </div>

                            <div class="receitainfo1">
                                <h4>Produzido com</h4>
                                <h2 class="descricaodrink">Amoras e Framboesas</h2>

                                <p class="descricaodrink">Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                                Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                                when an unknown printer took a galley of type and scrambled it to make a type 
                                specimen book.</p>

                                <a href="#" class="drink_botao2"> CONHEÇA NOSSA HISTÓRIA</a>
                            </div>
                        </div>

                        <div class="drink1">
                            <div class="receitas1">
                                <img class="receitaroxo" :src="receitaroxo"> 
                            </div>

                            <div class="receitainfo1">
                                <h4>Produzido com</h4>
                                <h2 class="descricaodrink">Baunilha e Groselha</h2>

                                <p class="descricaodrink">Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                                Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                                when an unknown printer took a galley of type and scrambled it to make a type 
                                specimen book.</p>

                                <a href="#" class="drink_botao3"> CONHEÇA NOSSA HISTÓRIA</a>
                            </div>
                        </div>

                        <div class="drink1">
                            <div class="receitas1">
                                <img class="receitaroxo" :src="drinkquatro"> 
                            </div>

                            <div class="receitainfo1">
                                <h4>Produzido com</h4>
                                <h2 class="descricaodrink">Canela e Gengibre</h2>

                                <p class="descricaodrink">Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                                Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                                when an unknown printer took a galley of type and scrambled it to make a type 
                                specimen book.</p>

                                <a href="#" class="drink_botao4"> CONHEÇA NOSSA HISTÓRIA</a>
                            </div>
                        </div>
                   </div>
            </div>
        <div @click="voltar02" class="botaod"><p>&gt;</p></div>
    </div>
</template>

<script>
    export default{
        name: "ReceitasDrinks",
        props:["receitalimao1", "receitavermelho", "receitaroxo", "drinkquatro"],

        data(){
            return{
                marginLeftDrink2: 0,
                contador: 1
            }
        },

        methods:{
            mover02(){
                if(this.marginLeftDrink2 == 0){
                    this.marginLeftDrink2 = -1200
                    this.contador ++
                    console.log('teste', this.contador)

                } else if(this.contador == 2){
                    this.marginLeftDrink2 = -2400
                    this.contador++
                    console.log('teste', this.contador)
                    
                } else if(this.contador == 3){
                    this.marginLeftDrink2 = -3590
                    this.contador++
                    console.log('teste', this.contador)
                }
            },
            
            voltar02(){
                if(this.contador == 4){
                    this.marginLeftDrink2 = -2400
                    this.contador--
                    console.log('teste', this.contador)

                } else if(this.contador == 3){
                    this.marginLeftDrink2 = -1200
                    this.contador--
                    console.log('teste', this.contador)

                } else if(this.contador == 2){
                    this.marginLeftDrink2 = 0
                    this.contador--
                    console.log('teste', this.contador)
                }
            }
        }

    }
</script>

<style>
     .areadrink{
        border-top: solid 0px blue;
        border-left: solid 0px blue;
        border-right: solid 0px blue;
        border-bottom: solid 3px rgb(170, 139, 59);
        height: 400px;
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .botaod{
        border: solid 2px rgb(170, 139, 59);
        width: 30px;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        transform: rotate(45deg);
        background-color: rgb(170, 139, 59);
        cursor: pointer;
    }

    .botaod p{
        transform: rotate(318deg);
    }

    .destaquedrink{
        background-color: rgba(4, 4, 14, 0.623);
        border: solid 0px blue;
        width: 1200px;
        height: 399px;
        overflow-x: hidden;
    }

    .destaque2{
        border: solid 0px black;
        border-right: solid 0px greenyellow ;
        width: 4795px;
        height: 396px;
        display: flex;
        transition: 0.8s;
    }

    .drink1{
        border: solid 0px greenyellow;
        width: 1198px;
        height: 399px;
        background-color: white;
        display: flex;
        justify-content: center;
    }

    .receitas1{
        border: solid 0px black;
        width: 40%;
        height: 396px;
        display: flex;
        justify-content: center;
    }

    .receitainfo1{
        border: solid 0px blue;
        width: 40%;
        height: 396px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .receitalimao1{
        width: 300px;
    }

    .receitavermelho{
        width: 300px;
        height: 340px;
        margin-top: 30px;
    }

    .receitaroxo{
        width: 250px;
        margin-top: 25px;
    }

    .descricaodrink{
        color: black;
        margin-top: -10px;
    }

    .drink_botao{
        width: 220px;
        height: 40px;
        background-color: green;
        border: solid 2px black;
        color: black;
        text-decoration: none;
        font-size: 13px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
    }

    .drink_botao2{
        width: 220px;
        height: 40px;
        background-color: rgb(153, 8, 44);
        border: solid 2px black;
        color: black;
        text-decoration: none;
        font-size: 13px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
    }

    .drink_botao3{
        width: 220px;
        height: 40px;
        background-color: rgb(102, 3, 116);
        border: solid 2px black;
        color: black;
        text-decoration: none;
        font-size: 13px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
    }

    .drink_botao4{
        width: 220px;
        height: 40px;
        background-color: rgb(155, 32, 2);
        border: solid 2px black;
        color: black;
        text-decoration: none;
        font-size: 13px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
    }

</style>