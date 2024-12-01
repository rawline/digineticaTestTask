<template>
   <div class="filterMenu">
        <CategoriesFilterMenu />
        <PriceFilterMenu />
        <BrandFilterMenu />
        <SizeFilterMenu />
   </div> 
</template>

<script>
import CategoriesFilterMenu from './filterMenuShared/CategoriesFilterMenu.vue';
import SizeFilterMenu from './filterMenuShared/SizeFilterMenu.vue';
import PriceFilterMenu from './filterMenuShared/PriceFilterMenu.vue';
import BrandFilterMenu from './filterMenuShared/BrandFilterMenu.vue';


export default {
  name: 'FilterMenu',
  components: {
    CategoriesFilterMenu,
    SizeFilterMenu,
    PriceFilterMenu,
    BrandFilterMenu,

   }
}

</script>

<style>
.filterMenu {
    width: 280px;
}

@media (max-width:1160px) {
   .filterMenu {
      display: none;
   }
}

</style>