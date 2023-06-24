<script>
    export default {
        
    }
</script>

<template>
    <div>
        <div class="container">
            <div class="d-flex">
                <div class="water pkm-type"></div>
                <div class="fire pkm-type"></div>
                <div class="grass pkm-type"></div>
                <div class="electric pkm-type"></div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.pkm-type{
    width: 30px;
    height: 30px;
    border-radius: 5rem;
    border: 2px solid white;
    margin: 1rem 0.5rem;
}

.water{
    width: 60px;
    height: 60px;
    border: 3px solid white;
    background: rgb(255,240,240);
    background: linear-gradient(123deg, rgba(255,240,240,1) 0%, rgba(0,9,129,1) 79%);
}
.grass{
    background: rgb(255,240,240);
    background: linear-gradient(123deg, rgba(255,240,240,1) 0%, rgba(0,120,30,1) 79%);
}
.electric{
    background: rgb(255,240,240);
    background: linear-gradient(123deg, rgba(255,240,240,1) 0%, rgba(242,232,4,1) 79%); 
}
.fire{
    background: rgb(255,240,240);
    background: linear-gradient(123deg, rgba(255,240,240,1) 0%, rgba(255,19,19,1) 79%);
}
</style>