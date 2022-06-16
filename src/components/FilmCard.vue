<template>
    <div class="card-container">
        <!-- Immagine copertina -->
        <img :src="'https://image.tmdb.org/t/p/' + 'w342' + filmObject.poster_path" :alt="filmObject.original_title">

        <!-- Titolo -->
        <div><span><b>Titolo:</b> {{filmObject.title}}</span></div>
        
        <h4>{{filmObject.name}}</h4>
        <!-- Titolo originale -->
        <div><span><b>Titolo originale:</b> {{filmObject.original_title}}</span></div>
        
        <!-- Lingua -->
        <div><span><b>Lingua originale:</b> {{filmObject.original_language}}</span></div>
              
        <!-- <img :src="'../assets/img/flag-' + filmObject.original_language + '.png'" :alt="filmObject.original_title"> -->
       
        <!-- Voto -->
        <div class="rate">
            <span><b>Voto:</b> </span>
            <font-awesome-icon icon="fa-solid fa-star" v-for="(i) in Math.ceil(filmObject.vote_average / 2)" :key="i"/>
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