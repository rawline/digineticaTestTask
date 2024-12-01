<template>
    <div class="sizeFilterMenu">
      <h2 class="sizeTitle">Размер</h2>

      <div class="sizesList" >
        <div class="sizeItem" v-for="i in 6" :key="i">
          <div class="checkboxAndName">
            <input type="checkbox" class="checkbox">
            <div class="sizeName">Атрибут</div>
          </div>
          <div class="sizeNameAmount">3</div>
        </div>
      </div>
    </div> 
 </template>
 
 <script>
 
 export default {
   name: 'SizeFilterMenu'
 }
 
 </script>
 
 <style>
 .sizeFilterMenu {
     width: 280px;
 }

 .sizeTitle {
    text-align: center;
    font-weight: bold;
    font-size: 16px;
 }

 .sizesList {
  margin-top: 16px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  height: 180px;
  overflow: scroll;
  overflow-x: hidden;
  padding-top: 5px;
}

.sizesList::-webkit-scrollbar {
  width: 5px;
}

.sizesList::-webkit-scrollbar-track {
  background: none;
  border-radius: 5px;
}

.sizesList::-webkit-scrollbar-thumb {
  background-color: var(--color-icons);
  border-radius: 5px;
}

.sizesList::-webkit-scrollbar-thumb:hover {
  background-color: #bbbbbb;
}

.sizeItem {
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

.sizeNameAmount {
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