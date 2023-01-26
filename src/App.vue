<script>
import axios from 'axios';
export default {
  name:'App',
  data(){
    return {
      baseUrl: 'http://127.0.0.1:8000/api/',
      movies: [],
    }
  },
  methods:{
    getApi(){
      axios.get(this.baseUrl + 'posts')
      .then(result =>{
        this.projects = result.data;
        console.log(this.projects);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}
</script>


<template>
  <h1>Main App Here</h1>
</template>


<style lang="scss">
@use './styles/general.scss';
</style>