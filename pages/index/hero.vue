<template lang="pug">
  .hero
    .c-container
      .o-grid
        .o-grid__row
          .o-grid__item.o-grid__item--sm-12
            .logo
              img(src="/logo.svg").logo-img
              .logotype SalesEQ
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
  @import "../../styles/_globals.scss";

  .hero {
    position: relative;
    min-height: rem(480);
    color: color('lightest');
    
    padding-top: space('xl');
    padding-bottom: space('xl');
    
    &::after {
      content: '';
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      top: 0;
      z-index: -1;
      
      transform: skewY(-10deg);
      transform-origin: 0;
      
      background-image: linear-gradient(
        to bottom, 
        color('primary'), 
        color('brand')
      );

      background-repeat: no-repeat;
    }
    
  }
  
  .logo {
    display: flex;
    align-items: center;
    justify-content: center;
    
    @include breakpoint('lg') {
      justify-content: flex-start;
    }
    
  }
  .logotype {
    font-size: 2rem;
    font-weight: 600;
    font-family: 'Avenir';
    margin-left: space('sm');
    text-shadow: 0 1px 2px color('brand');
  }
  .logo-img {
    filter: drop-shadow(0 1px 2px color('brand') );
    width: 3rem;
    height: 3rem;
  }

</style>
