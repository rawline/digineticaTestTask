<template>
    <div class="brandFilterMenu">
      <div class="titleBlock">
        <h2 class="brandBlockTitle">Бренд</h2>
        <a href="#" class="clearBtn">Очистить</a>
      </div>

      <div class="searchContainer">
          <img class="searchIcon" src="../../assets/icons/Mobile Icon.svg" alt="searchIcon">
          <input class="searchInput" type="text" placeholder="Поиск">
      </div>

      <div class="brandsList" >
        <div class="brandItem" v-for="i in 10" :key="i">
          <div class="checkboxAndName">
            <input type="checkbox" class="checkbox">
            <div class="brandName">Атрибут</div>
          </div>
          <div class="brandNameAmount">3</div>
        </div>
      </div>
    </div> 
 </template>
 
 <script>

 
 export default {
   name: 'BrandFilterMenu'
 }
 
 </script>
 
 <style>
.brandFilterMenu {
  width: 280px;
  margin-top: 28px;
}

.titleBlock {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brandBlockTitle {
    text-align: center;
    font-weight: bold;
    font-size: 16px;
 }

.clearBtn {
  font-size: 12px;
  color: var(--color-font-secondary);
}

 .searchContainer {
  position: relative;
  flex: 1;
}

.searchInput {
  width: 100%;
  height: 36px;
  padding: 8px 15px 8px 36px;
  box-sizing: border-box;
  font-size: 14px;
  border: solid var(--color-border) 1px;
  border-radius: 8px;
  outline: none;
}

.searchInput::placeholder {
  color: var(--color-font-secondary);
}

.searchIcon {
  position: absolute;
  left: 12px;
  top: 50%;
  transform: translateY(-50%);
  width: 16px;
  height: 16px;
  pointer-events: none;
}

.brandsList::-webkit-scrollbar {
  width: 5px;
}

.brandsList::-webkit-scrollbar-track {
  background: none;
  border-radius: 5px;
}

.brandsList::-webkit-scrollbar-thumb {
  background-color: var(--color-icons);
  border-radius: 5px;
}

.brandsList::-webkit-scrollbar-thumb:hover {
  background-color: #bbbbbb;
}

.brandsList {
  margin-top: 16px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  height: 180px;
  overflow: scroll;
  overflow-x: hidden;
  padding-top: 5px;
}

.brandItem {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-right: 16px;
  box-sizing: border-box;
  font-size: 14px;
  height: 20px;
}

.checkbox {
  appearance: none;
  position: relative;
  width: 20px;
  height: 20px;
  background: var(--color-white);
  border-radius: 3px;
  border: 1px solid #adadad;
}

.checkbox::after {
  content: "";
  position: absolute;
  width: 0px;
  height: 0px;
  top: 10px;
  left: 5px;
  transform: translateY(-50%);
  font-size: 30px;
  background-image: url("../../assets/icons/Vector.svg");
  background-repeat: no-repeat;
}

.checkbox:checked {
  background: var(--color-brand);
  border: none;
}

.checkbox:checked::after {
  width: 11px;
  height: 11px;
}

.brandNameAmount {
  font-size: 12px;
  transition: all 0.3s;
  color: var(--color-font-secondary);
}

.checkboxAndName {
  display: flex;
  gap: 12px;
  align-items: center;
}
 
 </style>