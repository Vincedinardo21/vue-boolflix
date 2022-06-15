<template>
    <section> 
        <div>
          <MySearch @miaRicerca="searchFilm"/>
          {{userText}} 
        </div> 
        <FilmCard v-for="(item, i) in films" :key="i" :filmObject="item"/>     
    </section>
</template>

<script>
import axios from "axios"
import FilmCard from "./FilmCard.vue";
import MySearch from "./MySearch.vue";

export default {
  name: 'FilmList',
  components: {
    FilmCard,
    MySearch,
  },
  data(){
    return {
        // API link
        apiUrl : "https://api.themoviedb.org/3/movie/550?api_key=a52d13991466b7a593490ce84099f0d3&language=en-US",
        films : [],
        userText : "",
    }
  },
  created(){
    this.getFilm();
  },
  methods: {
    getFilm(){
        axios.get(this.apiUrl).then((result) => {
            this.films.push(result.data);
            console.log(result);
        });
    },
    searchFilm(mytext){
      this.userText = mytext;
      console.log(mytext);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    section {
        min-height: 200px;
        background-color: aqua;
    }
</style>