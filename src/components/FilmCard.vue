<template>
    <div>
        <!-- Titolo -->
        <!-- <h2>Ciao</h2> -->
        <!-- Titolo originale -->
        <h2>{{filmObject.original_title}}</h2>
        <!-- Lingua -->
        <div></div>
        <!-- Voto -->
        <div></div>
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
    div {
        border: 1px solid black;
    }
</style>