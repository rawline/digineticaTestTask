<template>
    <div class="headerContainer">
        <div class="logoAndCatalog">
            <div class="logo">
                <img src="../assets/icons/material-symbols_image.svg" alt="logoIcon">
                <div class="logoText">Логотип</div>
            </div>
            <button class="catalogBtn">
                Каталог
            </button>
        </div>

        <div class="searchContainer">
            <img class="searchIcon" src="../assets/icons/SearchIcon.svg" alt="searchIcon">
            <img class="arrowLeftIcon" src="../assets/icons/arrowLeftIcon.svg" alt="arrowLeftIcon">
            <input class="searchInput" type="text" placeholder="Поиск по 100 000 товаров ">
            <button class="searchButton">Найти</button>
            <img src="../assets/icons/CancelIcon.svg" alt="cancelIcon" class="clearButton">   
        </div>

        <ol class="headerLinks">
            <li class="headerLink">Информация о компании</li>
            <li class="headerLink">Контакты</li>
            <li class="headerLink">Полезные ссылки</li>
        </ol>
    </div>
</template>

<script>
export default {
  name: 'TheHeader'
}
</script>

<style scoped>
* {
    font-family: 'Inter';
}
/* Общий стиль для header */
.headerContainer {
    height: 72px;
    display: flex;
    align-items: center;
    gap: 24px;
    padding: 12px 0;
    box-sizing: border-box;
}

.logoAndCatalog {
    display: flex;
    align-items: center;
    gap: 8px;
}

.logo {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 12px 24px 12px 24px;
    box-sizing: border-box;
}

.logoText {
    font-size: 16px;
}

.logo img {
    height: 24px;
    width: 24px;
}

.catalogBtn {
    display: flex;
    align-items: center;
    padding-left: 24px;
    padding-right: 24px;
    height: 48px;
    font-size: 14px;
    font-weight: 600;
    border: solid var(--color-brand) 1px;
    background-color: var(--color-white);
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s;
}

.catalogBtn:hover {
    color: #125BAE;
}

/* Секция поиска */
.searchContainer {
    position: relative;
    flex: 1;
}

.searchInput {
    width: 100%;
    height: 48px;
    padding: 8px 15px 8px 48px;
    box-sizing: border-box;
    font-size: 14px;
    border: solid var(--color-brand) 1px;
    border-radius: 8px;
    outline: none;
}

.searchInput::placeholder {
    color: #5A5A5A;
}

.searchIcon {
    position: absolute;
    left: 16px;
    top: 50%;
    transform: translateY(-50%);
    width: 24px;
    height: 24px;
    pointer-events: none;
}

.arrowLeftIcon{
    position: absolute;
    display: none;
}

.searchButton,
.clearButton {
    display: none;
}

.searchContainer:has(input:focus) .searchButton,
.searchContainer:has(input:focus) .clearButton {
    display: block;
}

.searchButton {
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    right: 4px;
    top: 50%;
    font-weight: 600;
    transform: translateY(-50%);
    width: 70px;
    height: 38px;
    font-size: 14px;
    color: var(--color-white);
    background-color: var(--color-brand);
    border: none;
    border-radius: 8px;
    cursor: pointer;
    box-sizing: border-box;
}

/* Кнопка очистить */
.clearButton {
    position: absolute;
    right: 78px;
    top: 50%;
    transform: translateY(-50%);
    height: 24px;
    width: 24px;
    cursor: pointer;
}

.searchButton,
.clearButton {
    display: none;
}

.searchContainer:has(input:focus) .searchButton,
.searchContainer:has(input:focus) .clearButton {
    display: block;
}

/* Секция ссылок */
.headerLinks {
    display: flex;
    gap: 20px;
    list-style: none;
    padding: 0;
    margin: 0;
}

.headerLink {
    font-size: 14px;
    color: #393939;
    cursor: pointer;
    transition: color 0.3s;
}

.headerLink:hover {
    color: #125BAE;
}

@media (max-width:1000px) {
   .logoAndCatalog, .headerLinks {
      display: none;
   }
}

@media (max-width:856px) {
    .searchContainer {
        padding: 0 16px 0 16px;
        position: relative;
    }
    .searchIcon {
        display: none;
    }
    .searchInput {
        width: 100%;
        height: 45px;
        padding: 8px 16px 0 0;
        box-sizing: border-box;
        margin-left: 36px;
        font-size: 16px;
        border: none;
        border-radius: 0;
        border-bottom: solid var(--color-border) 1px;
    }

    .arrowLeftIcon {
        display: block;
        top: 30%;
    }
}
</style>
