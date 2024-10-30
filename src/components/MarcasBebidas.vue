<template>
    <div class="areamarcas">
        <div class="marcas">
            <img class="lg1" :src="logo1">
            <img class="lg2" :src="logo2">
            <img class="lg3" :src="logo3">
        </div>
    </div>
</template>

<script>
    export default{
        name: "MarcasBebidas",
        props: ["logo1", "logo2", "logo3"],

        data(){
            return{

            }
        }
    }
</script>

<style>
    .areamarcas{
        border: solid 0px blue;
        border-bottom: solid 4px rgb(170, 139, 59);
        height: 200px;
        display: flex;
        justify-content: center;
        background-color: rgb(95, 95, 95);
    }

    .marcas{
        border: solid 0px white;
        width: 1200px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .lg1, .lg2, .lg3{
        width: 360px;
        height: 160px;
    }
</style>