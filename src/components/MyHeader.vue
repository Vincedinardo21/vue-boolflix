<template>
  <header>
      <h1>BOOLFLIX</h1>
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
    // border: 1px solid red;
    background-color: black;
    padding: 10px;

    h1 {
      color: red;
    }
  }
</style>
