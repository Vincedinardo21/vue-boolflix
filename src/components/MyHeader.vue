<template>
  <header>
    <div>
      <input type="search" placeholder="Scrivi qualcosa">
      <button>Cerca</button>
    </div>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header{
    min-height: 100px;
    border: 1px solid black;
  }
</style>
