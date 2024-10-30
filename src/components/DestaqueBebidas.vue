<template>
    <div class="areadestaque">
        <div @click="mover" class="botao"><p>&lt;</p></div>
            <div class="destaquebebidas">
                <div class="destaque" :style="{marginLeft: marginLeft + 'px'}">

                    <div class="bebidas">
                            <div class="lados1">
                                <img class="l1" :src="l1">
                            </div>

                            <div class="lados"><p>APROVEITE O DIA COM AMIGOS<br> <b>&</b> <br> JACK DANIELS </p> </div>
                            
                            <div class="lados2">
                                <img class="l2" :src="l2">
                            </div>
                    </div>
                    
                    <div class="bebidas2">
                            <div class="ladosb2-1"></div>
                            <div class="ladosb2"><p>APROVEITE O DIA COM AMIGOS<br> <b>&</b> <br> BOMBAY SAPPHIRE</p> </div>
                            <div class="ladosb2-2">
                                <img class="lb2-2" :src="lb22">
                            </div>
                    </div>

                    <div class="bebidas3">
                            <div class="ladosb3-1"></div>
                            <div class="ladosb3"><p>APROVEITE O DIA COM AMIGOS<br> <b>&</b> <br> TANQUERAY </p> </div>
                            <div class="ladosb3-2">
                                <img class="lb3-2" :src="lb33">
                            </div>
                    </div>

                    <div class="bebidas4">
                            <div class="ladosb4-1"></div>
                            <div class="ladosb4"><p>APROVEITE O DIA COM AMIGOS<br> <b>&</b> <br> CHIVAS REGAL </p> </div>
                            <div class="ladosb4-2">
                                <img class="lb4-2" :src="lb4">
                            </div>
                    </div>
                </div>    
            </div>
        <div class="botao"><p>&gt;</p></div>
    </div>
</template>

<script>
    export default{
        name: "DestaqueBebidas",
        props:['l1', 'l2', 'lb2', 'lb22', 'lb33', 'lb4'],

        data(){
            return{
                marginLeft: 6,
                contador: 0
            }
        },
        
        methods:{   
            mover(){
                this.marginLeft -=1200
            }
        },

        mounted(){
            const interval = 2000;
            let executionCount = 1;
            const maxExecutions = 3;

            const intervalId = setInterval(() =>{
                if(executionCount <= maxExecutions){
                this.mover();
                executionCount++
                console.log(executionCount)

                } /*else if(executionCount == 4){
                executionCount = 1;
                this.marginLeft +=3600
                } */else {
                clearInterval(intervalId);
                }
            }, interval)
        }
    }
</script>

<style>
    .areadestaque{
        border-top: solid 0px blue;
        border-left: solid 0px blue;
        border-right: solid 0px blue;
        border-bottom: solid 3px rgb(170, 139, 59);
        margin-top: -100px;
        height: 500px;
        background-color: rgb(10, 10, 10);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .botao{
        border: solid 2px white;
        width: 30px;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        transform: rotate(45deg);
        background-color: black;
        cursor: pointer;
    }

    .botao p{
        transform: rotate(318deg);
    }
    
    .destaquebebidas{
        background-color: rgba(4, 4, 14, 0.623);
        border: solid 0px blue;
        width: 1200px;
        height: 498px;
        overflow-x: hidden;
    }

    .destaque{
        border: solid 0px white;
        border-right: solid 0px greenyellow ;
        width: 4795px;
        height: 496px;
        display: flex;
        transition: 0.8s;
    }

                        /*--------JACK DANIELS--------*/
    .bebidas{
        border: solid 0px greenyellow;
        width: 1195px;
        height: 492px;
        display: flex;
        justify-content: space-between;
        align-items: end;
        background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('@/assets/bebida1.jpg');
        background-position: center;
        background-size: cover;
       }

    .lados{
        border: solid 0px white;
        width: 500px;
        height: 400px;
        font-size: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .lados1{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }
    
    .l1{
        width: 399px;
        height: 594px;
        margin-left: 0px;
        margin-top: 10px;
    }

    .lados{
        text-align: center;
    }

    .lados b{
        color: goldenrod;
        font-size: 55px;
    }

    .lados2{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }

    .l2{
        height: 480px;
        width: 296px;
        margin-top: 120px;
        transform: rotate(-20deg);
        margin-left: 100px;
    }

                        /*--------JACK DANIELS--------*/


                        /*--------BOMBAY SAPPHIRE--------*/
                        
    .bebidas2{
        border: solid 0px greenyellow;
        width: 1195px;
        height: 492px;
        display: flex;
        justify-content: space-between;
        align-items: end;
        background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), url('@/assets/bebida2.jpg');
        background-position: center;
        background-size: cover;
    }
    
    .ladosb2{
        border: solid 0px white;
        width: 500px;
        height: 400px;
        font-size: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    
    .ladosb2-1{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }
    
    .lb2-1{
        width: 399px;
        height: 594px;
        margin-left: 0px;
        margin-top: 10px;
    }

    .ladosb2{
        text-align: center;
    }
    
    .ladosb2 b{
        color: rgb(83, 94, 104);
        font-size: 55px;
    }
    
    .ladosb2-2{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }
    
    .lb2-2{
        height: 480px;
        width: 376px;
        margin-top: 70px;
        transform: rotate(-20deg);
        margin-left: 50px;
    }
    
                        /*--------BOMBAY SAPPHIRE--------*/
                        
                        /*--------TANQUERAY--------*/

    .bebidas3{
        border: solid 0px greenyellow;
        width: 1203px;
        height: 492px;
        display: flex;
        justify-content: space-between;
        align-items: end;
        background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), url('@/assets/bebida3.jpg');
        background-position: top;
        background-size: cover;
    }

    .ladosb3{
        border: solid 0px white;
        width: 500px;
        height: 400px;
        font-size: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .ladosb3-1{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }
    
    .lb3-1{
        width: 399px;
        height: 594px;
        margin-left: 0px;
        margin-top: 10px;
    }

    .ladosb3{
        text-align: center;
    }

    .ladosb3 b{
        color: green;
        font-size: 55px;
    }

    .ladosb3-2{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }

    .lb3-2{
        height: 530px;
        width: 506px;
        margin-top: 10px;
        transform: rotate(-40deg);
        margin-left: -40px;
    }

                        /*--------TANQUERAY--------*/
                        
                        /*--------CHIVAS REGAL--------*/

    .bebidas4{
        border: solid 0px greenyellow;
        width: 1195px;
        height: 492px;
        display: flex;
        justify-content: space-between;
        align-items: end;
        background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), url('@/assets/bebida4.1.jpg');
        background-position: top;
        background-size: cover;
    }

    .ladosb4{
        border: solid 0px white;
        width: 500px;
        height: 400px;
        font-size: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .ladosb4-1{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }
    
    .lb4-1{
        width: 399px;
        height: 594px;
        margin-left: 0px;
        margin-top: 10px;
    }

    .ladosb4{
        text-align: center;
    }

    .ladosb4 b{
        color: rgb(5, 77, 233);
        font-size: 55px;
    }

    .ladosb4-2{
        border: solid 0px white;
        width: 400px;
        height: 470px;
        overflow-y: hidden;
        overflow-x: hidden;
    }

    .lb4-2{
        height: 530px;
        width: 506px;
        margin-top: 20px;
        transform: rotate(-20deg);
        margin-left: -80px;
    }
</style>