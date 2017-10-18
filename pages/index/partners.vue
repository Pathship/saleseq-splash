<template lang="pug">
  .partners
    .c-container
      .o-grid
        .o-grid__row
          .o-grid__item.o-grid__item--sm-12
            h2.title We're trusted to deliver by these companies.
        .o-grid__row.o-grid__row--align-center.o-grid__row--justify-center
          .o-grid__item--sm-6.o-grid__item--md-4.o-grid__item--lg-2
            a(href="#").partner-logo
              img(src="/honey-logo.svg")
          .o-grid__item--sm-6.o-grid__item--md-4.o-grid__item--lg-2
            a(href="#").partner-logo
              img(src="/okta-logo.svg")
          .o-grid__item--sm-6.o-grid__item--md-4.o-grid__item--lg-2
            a(href="#").partner-logo
              img(src="/salesforce-logo.svg")
          .o-grid__item--sm-6.o-grid__item--md-4.o-grid__item--lg-2
            a(href="#").partner-logo
              img(src="/evernote-logo.svg")
          .o-grid__item--sm-6.o-grid__item--md-4.o-grid__item--lg-2
            a(href="#").partner-logo
              img(src="/trinet-logo.svg")
          .o-grid__item--sm-6.o-grid__item--md-4.o-grid__item--lg-2
            a(href="#").partner-logo
              img(src="/linkedin-logo.svg")
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
  @import "../../styles/_globals.scss";
  
  .partners {
    padding-top: space('md');
    padding-bottom: space('md');
  }

  .partner-logo {
    margin: 0 auto;
    margin-top: space('md');
    margin-bottom: space('md');
    transition: 175ms ease-in-out;
    
    display: flex;
    justify-content: center;
    align-content: center;
    
    width: rem(96);
    height: rem(96);
    border-radius: 40rem;
    box-shadow: 0 1px 2px rgba(0,0,0,.5);
    padding: space('md');
    border: .1rem solid color('blackhole');
    
    background-color: color('blackhole');
    background-image: linear-gradient(
      to bottom,
      color('darkest'),
      color('blackhole')
    );
    
    &:hover {
      cursor: pointer;
      opacity: 1;
      border: .1rem solid color('primary');
      filter: saturate(1.25);
    }
    
    img {
      width: 100%;
      object-fit: contain;
    }
    
    @include breakpoint('lg') {
      width: rem(128);
      height: rem(128);
    }
    
  }

  .title {
    font-weight: 600;
    font-size: 1.25rem;
    font-family: 'Avenir';
    line-height: 1.35;
    margin: 0 auto;
    text-shadow: 0 1px 1px rgba(0,0,0,.25);
    text-align: center;
    color: color('white');
    margin-top: space('lg');
    margin-bottom: space('md');
    
    @include breakpoint('lg') {
      text-align: right;
      margin: 0;
      margin-bottom: space('lg');
    }
  }

</style>
