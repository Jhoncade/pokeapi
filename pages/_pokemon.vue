<template>
    <div>
       <div class="stats">
        <p class="nombre">{{ nombre }}</p>
        <p v-for="i in pokemon.abilities" :key="i.name"> {{ i.ability.name }}</p>
        <p v-for="i in pokemon.stats" :key="i.stat.name"> {{ i.stat.name }} : {{ i.base_stat }}</p>
        <img v-bind:src="front" alt="">
       </div>
    </div>
</template>

<script>
export default{
    name: "pokemon_pagina",
    data(){
        return{
        pokemon: [],
        nombre: this.$route.params.pokemon,
        front: ""
        }
    },
    mounted(){
        this.getInfo()
    },
    methods: {
        async getInfo(){
        const {data}= await this.$axios.get(`pokemon/${this.$route.params.pokemon}`)
        this.pokemon=data
        console.log(data)
        console.log(this.route.params.pokemon)
        this.front=this.pokemon.sprites.other.dream_world.front_default

        },
        }
    
    }
    
    

</script>