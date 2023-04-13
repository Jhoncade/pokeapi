<template> 
  <div>
    <loading ></loading>
  </div>
    <!-- <div class="contenedortitulo" v-else>
      <h1 class="titulo">PokeDex</h1>
    <input type="text" class="buscar" v-model="search" v-on:keyup.enter="submit">
    
    
    <div  class="comtainer_carta">
      <card v-for="i in response" :key="i" :nombre="i.name" :url="i.images"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return{
      response: [],
      search: "",
      loading: true
    }
  },
  mounted(){
      this.getInfo()
  },
  methods: {
    async getInfo(){
    try {
      const {data}= await this.$axios.get('pokemon')
      let images = ""

      for (let i=0; i< data.results.length;i++){
        images=await this.getpokemon(data.results[i].name)
        data.results[i].images=images
      }
      this.response =data.results
      this.loading=false
    } catch (error) {
      console.log("error")
    }
    },
      async getpokemon(pokenombre){
        const{data} = await this.$axios.get(`pokemon/${pokenombre}`)
        return data.sprites.other["official-artwork"]["front_default"]
      }
  
  }
  
}
</script>

<style>
.contenedortitulo{
  background-color: rgba(0, 0, 0, 0.849);
  margin-bottom: 15px;
  padding-bottom: 15px;
}
.titulo{
  color: white;
  
  padding: 10px 0;
  text-align: center;
  font-weight: 700;
  font-size: 55px;
}
.buscar{
  height: 35px;
  width: 350px;
  margin-left: 10px;
}
.comtainer_carta{
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}
h1{
  color: black;
}
div{
  background-color: red;
  margin: auto;
}
</style> -->
