# Family.scss
Family.scss - это набор Sass-миксинов, которые помогут вам легко управлять стилем n-го дочернего элемента.

> Данная версия является копией оригинального проекта [Lucas Bonomi](https://github.com/LukyVj), адаптированного для использования в Kalium19.

## Пример использования
```scss
// Sass (SCSS) input
ul li {
  background: blue;

  @include first(3) {
    background: blue;
  }
}
```
```css
/* CSS Output */
ul li {
  background: blue;
}
ul li:nth-child(-n + 3) {
  background: blue;
}
```
