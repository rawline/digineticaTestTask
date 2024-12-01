<template>
    <div class="cardWrapper">
        <div class="cardImg">
            <div class="hitOfSales">
                <div class="hitOfSalestext">
                    Хит продаж
                </div>
                <img src="../assets/icons/fireIcon.svg" alt="fireSvg">
            </div>
            <img src="../assets/icons/boxIcon.svg" alt="boxIcon" class="boxIcon">
            <div class="salesBox">
                25%
            </div>
        </div>

        <h3 class="cardCategory">Бренд</h3>
        <div class="cardDescr">Полное название товара в несколько строк для вида с обрывом в конце...</div>
        <div class="cardPriceWrapper">
            <h2 class="actualPrice">5 990 ₽</h2>
            <h4 class="priceBefore">5 990 ₽</h4>
        </div>
        <button class="cardBtn">Купить</button>
    </div>

</template>

<script>
export default {
    name: 'CardComponent',
}
</script>

<style>

.cardWrapper {
    max-width: 333px;
    cursor: pointer;
}

.cardImg {
    padding: 12px;
    box-sizing: border-box;
    display: block;
    width: 100%;
    height: 200px;
    background-color: #F8F8FA;
    position: relative;
    margin-bottom: 16px;
}

.boxIcon {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: all 0.3s;
}

.cardWrapper:hover .boxIcon {
    width: 82px;
    height: 82px;
}


.hitOfSales {
    width: 116px;
    height: 32px;
    display: flex;
    align-items: center;
    background-color: var(--color-white);
    border: solid var(--scroll-bar) 1px;
    padding: 6px 8px;
    box-sizing: border-box;
    border-radius: 4px;
    gap: 4px;
}

.hitOfSalestext {
    font-size: 14px;
}

.salesBox{
    width: 48px;
    height: 26px;
    font-size: 14px;
    font-weight: bold;
    background-color: var(--color-brand);
    color: var(--color-white);
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 4px;
    position: absolute;
    bottom: 12px;
    left: 12px;
}

.cardCategory {
    margin: 0;
    color: var(--color-font-secondary);
    font-size: 14px;
    margin-bottom: 8px;
}

.cardDescr {
    font-size: 14px;
    margin-bottom: 16px;
}

.cardDescr:hover {
    color: var(--color-font-hover);
    cursor: pointer;
}

.cardPriceWrapper {
    display: flex;
    align-items: center;
    gap: 8px;
}

.actualPrice {
    font-weight: bold;
    font-size: 16px;
}

.priceBefore {
    font-size: 12px;
    font-weight: normal;
    color: var(--color-font-secondary);
    text-decoration: line-through;
}

.cardBtn {
    padding: 12px 16px;
    background-color: var(--color-white);
    outline: none;
    border: solid var(--color-brand) 1px;
    color: var(--color-brand);
    font-size: 14px;
    font-weight: bold;
    border-radius: 4px;
    transition: all 0.3s;
    cursor: pointer;
}

.cardBtn:hover {
    background-color: var(--color-brand);
    color: var(--color-white);
}



</style>