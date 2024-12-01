<template>
     <ol class="categoriesList">
         <li class="mainCategory">
             <div class="categoriesWrapper">
                 Название категории
                 <span class="categoriesCount">3</span>
             </div>
             <ol class="innerCategories">
                 <li>
                     <div class="categoriesWrapper">
                         Название категории
                         <span class="categoriesCount">3</span>
                     </div>
                 </li>
                 <li>
                     <div class="categoriesWrapper">
                         Название категории
                         <span class="categoriesCount">3</span>
                     </div>
                 </li>
                 <li>
                     <div class="categoriesWrapper">
                         Название категории
                         <span class="categoriesCount">3</span>
                     </div>
                 </li>
             </ol>
         </li>
     </ol>
 </template>
 
 <script>
 export default {
   name: 'CategoriesFilterMenu',
 }
 
 </script>
 
 <style scoped>
 ol {
     list-style: none;
 }
 
 .categoriesWrapper {
     height: 30px;
     display: flex;
     align-items: center;
     justify-content: space-between;
     border-radius: 5px;
     transition: all 0.3s;
     cursor: pointer;
     font-size: 14px;
     padding: 7px 16px 7px 8px;
     box-sizing: border-box;
 }
 
 .categoriesWrapper:hover {
     background-color: var(--color-font-bg);
 }
 
 .categoriesWrapper:hover .categoriesCount {
     color: var(--color-font-main);
 }
 
 .categoriesCount {
    font-size: 12px;
     transition: all 0.3s;
     color: var(--color-font-);
 }
 

 .categoriesList {
     margin: 0;
     padding: 0;
 }
 
 </style>