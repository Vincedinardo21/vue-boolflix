<template>
    <section> 
        <div>
          <MySearch @miaRicerca="searchFilm"/>
          <!-- {{userText}}  -->
        </div> 
        <div class="film-container">
            <FilmCard v-for="(item, i) in films" :key="i" :filmObject="item"/>
        </div>
        
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
        apiUrl : "https://api.themoviedb.org/3/search/movie?api_key=a52d13991466b7a593490ce84099f0d3&query=",
        upiUrlSerie : "https://api.themoviedb.org/3/search/tv?api_key=a52d13991466b7a593490ce84099f0d3&query=",
        films : [],
        // series : [],
        userText : "back to the future",
    }
  },
  created(){
    this.getFilm();
    this.getSerie();
  },
  methods: {
    getFilm(){
        axios.get(this.apiUrl + this.userText).then((result) => {
            this.films = result.data.results;
            console.log(result);
        });
    },
    getSerie(){
        axios.get(this.apiUrlSerie + this.userText).then((result) => {
            this.films = result.data.results;
            console.log(result);
        });
    },
    searchFilm(mytext){
      this.userText = mytext;
      console.log(mytext);
      this.getFilm();
      this.getSerie();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    section {
        min-height: 200px;
        background-color: gray;
        

        .film-container {
          display: flex;
          flex-wrap: wrap;
          width: 95%;
          margin: 0 auto;
        }
    }
</style>