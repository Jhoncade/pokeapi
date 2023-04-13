<template>
    <NuxtLink :to="nombre" class="container">
        <img v-bind:src="url" alt="imagen">
        <p class="nombre">{{nombre}}</p>
    </NuxtLink>
</template>

<script>

export default{
    name: "CardComponent",
    props: {
        nombre: {
            type: String,
            required: true
        },
        url: {
            type: String,
            required: true
        }
    }
    }
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    
}

.container{
    height: 250px;
    width: 250px;
    border: 1px solid white;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    padding: 25px 0;
}
.nombre{
    font-size: 18px;
    color: white;
    
}
img{
    height: 150px;
    width: 200px;
}
</style>