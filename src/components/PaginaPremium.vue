<template>
    <div class="areapremium">
        <div class="premium">
            <div class="premium01">
                <div class="imagemcopo"></div>
                <div class="descricaocopo">
                    <p class="descricaop">Premium Blended Malt</p>
                    <h2 class="outras">OUTRAS MARCAS</h2>

                    <p >Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                    Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                    when an unknown printer took a galley of type and scrambled it 
                    to make a type specimen book.</p> 

                    <a class="distri" href="#">DISTRIBUIDORES</a>
                </div>
            </div>

            <div class="premium02">
                <div class="litro1">
                    <img class="civas" :src="civas">
                    <h3>CHIVAS REGAL</h3>
                    <p class="descrito">PREMIUM BLENDED</p>
                </div>

                <div class="litro2">
                    <img class="jack" :src="jack">
                    <h3>JACK DANIELS</h3>
                    <p class="descrito">NO 7 BRAND</p>
                </div>

                <div class="litro3">
                    <img class="johny" :src="johny">
                    <h3>JOHNNIE WALKER</h3>
                    <p class="descrito">BLACKLABBEL</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: "PaginaPremium",
        props: ["civas", "jack", "johny"],

        data(){
            return{

            }
        }
    }
</script>

<style>
    .areapremium{
        border: solid 0px blue;
        height: 400px;
        display: flex;
        justify-content: center;
    }

    .premium{
        border: solid 0px white;
        width: 1200px;
        height: 398px;
        display: flex;
    }

    .premium01{
        border: solid 0px orange;
        width: 50%;
        display: flex
    }

    .imagemcopo{
        width: 900px;
        height: 99%;
        border: solid 0px greenyellow;
        background-image: url('@/assets/bebidapremium.png');
        background-position: center;
        background-size: cover;
    }

    .premium02{
        border: solid 0px green;
        width: 50%;
        display: flex;
        justify-content: space-evenly;
    }

    .descricaocopo{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .outras{
        position: relative;
        margin-top: -10px;
    }

    .distri{
        text-decoration: none;
        border: solid 0px gray;
        color: black;
        background-color: white;
        width: 180px;
        height: 35px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .descricaop{
        color: greenyellow;
    }

    .litro1, .litro2, .litro3{
        border: solid 0px white;
        width: 155px;
        height: 393px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .civas{
        height: 300px;  
    }

    .jack{
        height: 300px;
    }

    .johny{
        height: 300px;
    }
    
    .descrito{
        position: relative;
        margin-top: -10px;
    }

    
</style>