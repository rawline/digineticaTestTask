# Тестовое задание для компании DIGINETICA
## Задание один
```
function getProductMiniCardValues() {
    const productElements = document.querySelectorAll('._product');
    const miniCardValues = Array.from(productElements).map(el => el.getAttribute('data-product-mini-card'));
    console.log(miniCardValues);
    return miniCardValues;
}

getProductMiniCardValues();
```
## Задание два
```
function extractProductAttributes() {
    const attributes = {};
    const items = document.querySelectorAll('.tab-pane-product-parameter-item');

    items.forEach(item => {
        const nameElement = item.querySelector('.parameter-name');
        const valueElement = item.querySelector('.parameter-value');

        if (nameElement && valueElement) {
            const name = nameElement.childNodes[0].nodeValue.trim();
            const value = valueElement.textContent.trim();
            attributes[name] = value;
        }
    });

    console.log(attributes);
    return attributes;
}

extractProductAttributes();
```
# Команды для запуска проекта с версткой
## Установка зависимостей проекта
```
npm install
```

### Команда для компиляции и запуска проекта на локальном сервере
```
npm run serve
```

### Команда для билда проекта
```
npm run build
```
