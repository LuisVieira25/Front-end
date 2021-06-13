<template>
  <div class="hello">
    
    <div v-for="(item, index) in resultados" :key="index">
        <h3>{{item}}</h3>
        <img :src="item" alt="">
        
    </div>
  </div>
</template>

<script>
import axios from "axios"

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      resultados: ""
    }
  },
  methods:{
    carregaInfo(query){
      //axios.get('https://images-api.nasa.gov/search?q='+query+'&media_type=image')
      axios.get('https://dog.ceo/api/breed/'+query+'/images')
        .then(
          res => {
            this.resultados = res.data.message//res.data.collection.items
          }
        )
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
