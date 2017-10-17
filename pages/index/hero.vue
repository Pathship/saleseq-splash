<template lang="pug">
  .hero
    .c-container
      .o-grid
        .o-grid__row
          .o-grid__item.o-grid__item--sm-12
            .logo
              img(src="/logo-grad-shadow.svg").logo-img
              .logotype SalesEQ
            h1.title Call more. Learn more. Close more.
        .o-grid__row
          .o-grid__item.o-grid__item--sm-12
            .cta-container
              .cta.cta-primary Get smarter
              .cta.cta-secondary Learn more
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
  @import "../../styles/_globals.scss";

  .hero {
    position: relative;
    color: color('lightest');
    
    padding-top: space('xxl');
    padding-bottom: space('xxl');
    
    &::after {
      content: '';
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      top: 0;
      z-index: -1;
      
      background-image: linear-gradient(
        to bottom left, 
        color('off-primary'),
        color('primary')
      );

      filter: drop-shadow(0 1px 2px #000);
    }
    
  }
  
  .logo {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    
    @include breakpoint('lg') {
      justify-content: flex-start;
    }
    
  }
  .logotype {
    font-size: 1.5rem;
    font-weight: 600;
    font-family: 'Avenir';
    margin-left: space('sm');
    text-shadow: 0 1px 1px rgba(0,0,0,.25);
  }
  .logo-img {
    filter: drop-shadow(0 1px 1px rgba(0,0,0,.25) );
    width: 3rem;
    height: 3rem;
    padding: .5rem;
    border-radius: 6rem;
    background-color: color('white');
  }
  
  .title {
    margin-top: space('xxl');
    font-size: 3rem;
    font-weight: 600;
    font-family: 'Avenir';
    text-shadow: 0 1px 1px rgba(0,0,0,.25);
  }
  
  .cta-container {
    padding-top: space('xl');
    display: flex;
  }
  
  .cta {
    padding: space('md') space('lg');
    border-radius: 4px;
    border: .1rem solid transparent;
    font-weight: 600;
    font-size: 1rem;
    font-family: monospace;
    cursor: pointer;
    box-shadow: 0 1px 2px rgba(0,0,0,0);
    transition: 200ms ease-in-out box-shadow;
    
    & + & { margin-left: space('md'); }
    
    &.cta-primary {
      background-color: transparent;
      border-color: currentColor;
    }
    
    &.cta-secondary {
      background-color: color('white');
      color: color('primary');
    }
    
    &:hover {
      box-shadow: 0 2px 6px rgba(0,0,0,.25);
    }
    
  }

</style>
