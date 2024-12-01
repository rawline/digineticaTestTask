<template>
  <div class="container">
    <TheHeader />
    <section class="mainSection">
      <FilterMenu />
      <section class="products">
        <ProductCard v-for="i in 12" :key="i" />
      </section>
    </section>
  </div>
</template>

<script>
import TheHeader from './components/Header.vue'
import FilterMenu from './components/FilterMenu.vue';
import ProductCard from './components/ProductCard.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    FilterMenu,
    ProductCard
  }
}
</script>

<style>
:root {
    --color-font-main: #333333;
    --color-font-hover: #125BAE;
    --color-font-secondary: #AAAAAA;
    --color-font-bg: #E2EFFF;
    --color-brand: #7397F5;
    --color-border: #D5D5D5;
    --scroll-bar: #F2F2F2;
    --color-icons: #CBCBCB;
    --color-white: #fff;
}

* {
  font-family: 'PT Sans', sans-serif;
  color: var(--color-font-main);
  font-weight: 400;
}

body {
  margin: 0;
  padding: 0 100px;
}

.mainSection {
  max-width: 1720px;
  display: flex;
  margin-top: 24px;
  gap: 36px;
  margin-bottom: 20px;
}

.products {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
  width: 100%;
}

@media (max-width:856px) {
   body {
    padding: 0 30px;
   }

   .products {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
      width: 100%;
    }
}

@media (max-width:375px) {
   body {
    padding: 0;
   }

   .products {
      padding: 0 16px;
    }
}
</style>
