<template>
    <div class="card-container">
        <!-- Immagine copertina -->
        <img :src="'https://image.tmdb.org/t/p/' + 'w342' + filmObject.poster_path" :alt="filmObject.original_title">

        <!-- Titolo -->
        <h2>{{filmObject.title}}</h2>
        <h2>{{filmObject.name}}</h2>
        <!-- Titolo originale -->
        <h3>{{filmObject.original_title}}</h3>
        <!-- Lingua -->
        <div>{{filmObject.original_language}}</div>      
        <!-- <img :src="'../assets/img/flag-' + filmObject.original_language + '.png'" :alt="filmObject.original_title"> -->
       
        <!-- Voto -->
        <div>{{filmObject.vote_average}}</div>
        <div>{{Math.ceil(filmObject.vote_average / 2)}}</div>
        <div class="rate" v-for="(i) in Math.ceil(filmObject.vote_average / 2)" :key="i">
            <!-- <span>Star</span> -->
            <font-awesome-icon icon="fa-solid fa-star" />
        </div>
    </div>
</template>

<script>
export default {
  name: 'FilmCard',
  props: {
      filmObject : Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .card-container {
        width: 342px;
        border: 1px solid black;
    }
</style>