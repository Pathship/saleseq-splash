<template lang="pug">
  .hero
    .c-container
      .o-grid
        .o-grid__row.o-grid__row--align-center
          .o-grid__item.o-grid__item--sm-12
            .logo
              img(src="/logo-grad-shadow.svg").logo-img
              .logotype SalesEQ
        .o-grid__row.o-grid__row--align-center
          .o-grid__item.o-grid__item--sm-12.o-grid__item--lg-6
            h1.title Call more. Learn more. Close more.
            h2.sub-title Get stellar sales performance using technology that truly understands how your prospects think &amp; feel.
          .o-grid__item.o-grid__item--sm-12.o-grid__item--lg-5.o-grid__item--lg-push-1
            
        .o-grid__row
          .o-grid__item.o-grid__item--sm-12
            .cta-container
              .cta.cta-primary
                span Get smarter
              .cta.cta-secondary
                span Learn more
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
      
      background-image: linear-gradient(
        to bottom left, 
        color('off-primary'),
        color('primary')
      );

      filter: drop-shadow(0 1px 2px #000);
      
      transform: skewY(-4deg);
      transform-origin: 0;
    }
    
    @include breakpoint('lg') {
      padding-top: space('xxl');
      padding-bottom: space('xxl');
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
    margin-left: space('md');
    text-shadow: 0 1px 1px rgba(0,0,0,.25);
  }
  .logo-img {
    filter: drop-shadow(0 1px 1px rgba(0,0,0,.25) );
    width: 3rem;
    height: 3rem;
    padding: .5rem;
    border-radius: 6rem;
    
    background-color: color('white');
    background-image: linear-gradient(
      to bottom,
      color('white'),
      color('lighter')
    )
  }
  
  .title {
    font-size: 2.75rem;
    font-weight: 600;
    font-family: 'Avenir';
    text-shadow: 0 1px 1px rgba(0,0,0,.25);
    max-width: rem(420);
    text-align: center;
    margin: 0 auto;
    margin-top: space('xl');
    
    @include breakpoint('lg') {
      text-align: left;
      font-size: 3rem;
      margin: 0;
      max-width: rem(480);
      margin-top: space('xxl');
    }
  }
  
  .sub-title {
    font-weight: 400;
    font-size: 1.35rem;
    line-height: 1.35;
    max-width: rem(480);
    margin: 0 auto;
    text-shadow: 0 1px 1px rgba(0,0,0,.25);
    opacity: .9;
    text-align: center;
    margin-top: space('md');
    
    @include breakpoint('lg') {
      text-align: left;
      margin: 0;
      margin-top: space('md');
    }
  }
  
  .cta-container {
    padding-top: space('xl');
    display: flex;
    justify-content: center;
    
    @include breakpoint('lg') {
      justify-content: flex-start;
    }
  }
  
  .cta {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: space('sm') space('md');
    border-radius: 4px;
    border: .05rem solid transparent;
    font-weight: 500;
    font-size: 1rem;
    font-family: 'Avenir';
    cursor: pointer;
    box-shadow: 0 1px 2px rgba(0,0,0,0);
    transition: 125ms ease-in-out;
    
    & + & { margin-left: space('md'); }
    
    &.cta-primary {
      background-color: transparent;
      border-color: currentColor;
      
      &:hover {
        background-color: rgba(0,0,0,.1);
      }
      
    }
    
    &.cta-secondary {
      background: color('white');
      color: color('primary');
    }
    
    &:hover {
      box-shadow: 0 2px 6px rgba(0,0,0,.25);
    }
    
    @include breakpoint('lg') {
      padding: space('md') space('lg');
    }
    
  }
  
  .hero-box {
    background-color: #fff;
    padding: space('md');
    border-radius: 8px;
    box-shadow: 0 1px 2px rgba(0,0,0,.25);
    width: 100%;
    height: auto;
    overflow: hidden;
  }

</style>
