<template>
  <div id="app">
    <MyHeader/>

    <main>
      <FilmList/>
    </main>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import FilmList from './components/FilmList.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    FilmList,
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  //text-align: center;
  color: #2c3e50;
  //margin-top: 60px;
}
</style>
