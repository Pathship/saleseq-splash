<template lang="pug">
  .v-index
    index-hero
</template>

<script>
import IndexHero from './index/hero'

export default {
  name: 'v-index',
  components: {
    IndexHero
  }
}
</script>

<style lang="scss" scoped>
  @import "../styles/_globals.scss";
  
  .v-index {

  }
</style>
