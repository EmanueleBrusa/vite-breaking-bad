<script>
    export default {
        props:{
            MyPokemon : Object
        }
    }
</script>

<template>
    <div class="card-wrapper">
        <div class="d-flex align-items-center flex-column card mb-4 " :class="MyPokemon.type1 === 'Grass'? 'green-bkg' : MyPokemon.type1 === 'Water' ? 'blue-bkg' : MyPokemon.type1 === 'Fire'? 'red-bkg': ''">
            <img :src="MyPokemon.imageUrl" alt=""/>
            <div>{{ MyPokemon.number }}</div>
            <h5 class="card-title">{{ MyPokemon.name }}</h5>
            <p class="card-text">{{ MyPokemon.type1 }} </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
img{
   width: 100px;
   height: 100px;
   border-radius: 50%;
   margin-top: 10px;
}
.green-bkg{
    background-color: #DEFDE0;
}
.blue-bkg{
    background-color: #DEF3FD
}
.red-bkg{
    background-color: #FDDFDF;
}
.card-text{
    padding-bottom: 10px;
}
.card:hover{
    cursor: pointer;
}
</style>