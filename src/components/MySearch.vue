<template>
    <div>
        <input type="search" placeholder="Scrivi qualcosa" v-model="inputText" @keyup.enter="$emit('miaRicerca', inputText)">
        <button @click="$emit('miaRicerca', inputText)">Cerca</button>
    </div>
</template>

<script>
export default {
  name: 'MySearch',
  data(){
    return {
        inputText : "",
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  
</style>