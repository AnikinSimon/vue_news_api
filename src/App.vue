<template>
  <div id="app">
  </div>
</template>

<script>

export default {
  name: 'App',
  
  methods:{
      getData(){
        this.axios.get('https://newsapi.org/v2/top-headlines?country=us&apiKey=d7f41a32c26b4bbfb596d58b1a54c766')
          .then((response)=>{
            console.clear()
            let info = response.data.articles
            console.log(info)
          })
      }
    },
    mounted(){
      this.getData();
    }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
