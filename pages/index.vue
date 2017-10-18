<template lang="pug">
  .v-index
    index-hero
    index-partners
</template>

<script>
import IndexHero from './index/hero'
import IndexPartners from './index/partners'

export default {
  name: 'v-index',
  components: {
    IndexHero,
    IndexPartners
  }
}
</script>

<style lang="scss" scoped>
  @import "../styles/_globals.scss";
  
  .v-index {
    
  }
</style>
