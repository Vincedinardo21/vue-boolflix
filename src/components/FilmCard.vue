<template>
    <div class="card-container">
        <!-- Immagine copertina -->
        <img :src="'https://image.tmdb.org/t/p/' + 'w342' + filmObject.poster_path" :alt="filmObject.original_title">

        <div class="text-container">
            <!-- Titolo -->
            <div><span><b>Titolo:</b> {{filmObject.title}}</span></div>
        
            <!-- <h4>{{filmObject.name}}</h4> -->
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

            <!-- Overview -->
            <div><span><b>Overviev:</b> {{filmObject.overview}}</span></div>
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
        width: 344px;
        border: 1px solid white;
        margin: 5px;
        position: relative;
        background-color: black;

        .text-container {
            display: none;
            position: absolute;
            top: 0;
            padding: 10px;
            color: gray;

            b {
                color: white;
            }
            .fa-star {
                color:goldenrod;
            }
        }

        &:hover{
            .text-container {
                // border: 2px solid red;
                display: block;
            }

            img {
                opacity: 10%;
            }
        }       
    }
</style>