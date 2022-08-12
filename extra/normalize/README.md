# normalize.css

<a href="https://github.com/necolas/normalize.css">
  <img src="https://necolas.github.io/normalize.css/logo.svg" alt="Normalize Logo" width="80" height="80" align="right">
</a>

A modern alternative to CSS resets

> [Normalize.css](https://github.com/necolas/normalize.css) — это небольшой CSS-файл, который обеспечивает для HTML-элементов лучшую кроссбраузерность в стилях по умолчанию. Это современная, готовая к HTML5 альтернатива традиционному reset.css.

## Что он делает?

* Сохраняет полезные значения по умолчанию, в отличие от многих сбросов CSS.
* Нормализует стили для широкого спектра элементов.
* Исправляет ошибки и распространенные несоответствия браузера.
* Улучшает удобство использования с помощью незначительных изменений.
* Объясняет, что делает код, используя подробные комментарии.


## Поддержка браузеров

* Chrome
* Edge
* Firefox ESR+
* Internet Explorer 10+
* Safari 8+
* Opera


## Extended details and known issues

Additional detail and explanation of the esoteric parts of normalize.css.

### `pre, code, kbd, samp`
Хак `font-family: monospace, monospace` исправляет наследование и масштабирование
размера шрифта для предварительно отформатированного текста. Дублирование `monospace` является
преднамеренным. [Источник](https://en.wikipedia.org/wiki/User:Davidgothberg/Test59 ).

### `sub, sup`
Обычно использование `sub` или `sup` влияет на высоту строки текста во всех
браузерах. [Источник](https://gist.github.com/413930 ).

### `select`
По умолчанию Chrome в OS X и Safari в OS X допускают очень ограниченный стиль
`select`, если не задано свойство border. Вес шрифта по умолчанию в `optgroup`
элементы не могут быть безопасно изменены в Chrome на OSX и Safari на OS X.

### `[type="checkbox"]`
Рекомендуется не стилизовать флажки и радио инпуты, поскольку
реализация Firefox не учитывает `box-sizing`, `padding` или `width`.

### `[type="number"]`
Определенные значения размера шрифта, применяемые к числовым вводам, приводят
к изменению стиля курсора кнопки уменьшения с `default` на `text`.

### `[type="search"]`
По умолчанию вводимые данные поиска не полностью стилизуются. В Chrome и Safari на
OSX / iOS вы не можете управлять`font`, `padding`, `border` или `background`. В
Chrome и Safari в Windows вы не можете правильно управлять свойством `border`. Это будет применяться к
`border-width`, но будет отображаться только цвет границы (который нельзя контролировать)
для внешнего `1px` этой границы. Применение `-webkit-appearance: textfield`
устраняет эти проблемы, не устраняя преимуществ ввода данных поиска (например
, отображение прошлых поисковых запросов).
