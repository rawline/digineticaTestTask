<template>
    <div class="priceFilterMenu">
        <h2 class="priceTitle">Цена</h2>
        <div class="priceInputs">
            <div class="inputContainer">
                <span>от</span>
                <input type="number" class="priceInput priceMin">
            </div> 
            <img src="../../assets/icons/Divider.svg" alt="dividerIcon">
            <div class="inputContainer">
                <span>от</span>
                <input type="number" class="priceInput priceMax">
            </div> 
        </div>
    </div> 
 </template>
 
 <script>
 
 export default {
   name: 'PriceFilterMenu'
 }
 
 </script>
 
 <style>
 * {
    font-family: 'PT Sans';
}
 .priceFilterMenu {
    width: 280px;
 }

 .priceTitle {
    text-align: center;
    font-weight: bold;
    font-size: 16px;
 }

 .priceInputs {
    display: flex;
    align-items: center;
    justify-content: space-between;
 }

 .inputContainer {
    display: flex;
    align-items: center;
    width: 120px;
    height: 36px;
    border-radius: 4px;
    border: solid 1px var(--color-border);
    padding: 11px 0 11px 8px;
    gap: 6px;
    box-sizing: border-box;
 }

 .priceInput {
    width: 100%;
    border: none;
    outline: none;
    position: relative;
    font-size: 14px;
 }


 span {
    color: var(--color-font-secondary);
    font-size: 12px
 }

 .priceInput::placeholder {
    position: absolute;
 }
 
 </style>