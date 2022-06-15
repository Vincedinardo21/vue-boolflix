<template>
  
</template>

<script>
import axios from "axios"

export default {
  name: 'FilmList',
  components: {
    FilmCard,
  },
  data(){
    return {
        // API link
        apiUrl : "https://api.themoviedb.org/3/movie/550?api_key=a52d13991466b7a593490ce84099f0d3",
        films : []
    }
  },
  create(){
    this.getFilm();
  },
  methods: {
    getFilm(){
        axios.get(this.apiUrl).then((result) => {
            this.films = result.data.response;
            console.log(result);
        });
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  
</style>