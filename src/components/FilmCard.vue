<template>
    <div class="card-container">
        <!-- Titolo -->
        <h2>{{filmObject.title}}</h2>
        <!-- Titolo originale -->
        <h3>{{filmObject.original_title}}</h3>
        <!-- Lingua -->
        <div>{{filmObject.original_language}}</div>
        <!-- Voto -->
        <div>{{filmObject.popularity}}</div>
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
        width: 300px;
        border: 1px solid black;
    }
</style>