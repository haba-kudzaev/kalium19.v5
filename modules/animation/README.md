# `animation()`
Миксин `animation()` является лишь обёрткой над миксином `prefixer()`, который всего-то добавляет CSS-свойству `animation` браузерные префиксы, список которых прописан в файле [modules/_config.scss](https://github.com/91muilak/kalium19/blob/develop/modules/_config.scss) (в нашем случае префиксы прописаны в переменной `$prfxs_animation`).

> CSS-свойство `animation` это короткая запись для `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode` и `animation-play-state`
>
> [Подробнее на MDN →](https://developer.mozilla.org/ru/docs/Web/CSS/animation)

## Синтаксис миксина
- `$params...` - список значений без запятой
```scss
animation($params...)
```

## Пример использования
```scss
.block {
  ...
  @include animation(myFrames 3s ease-in-out infinite);
}

@include keyframes(myFrames) { ... }
```

# `animation-delay()`
Миксин `animation-delay()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-delay` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-delay`).

> Свойство `animation-delay` устанавливает время ожидания перед запуском цикла анимации. Значение `0s` или `0ms` запускает анимацию сразу же. Отрицательное значение также включает анимацию без задержек, но может привести к изменению вида начала анимации.
>
> [Подробнее на WebRef →](https://webref.ru/css/animation-delay)

## Синтаксис миксина
- `$delay` - время задержки
```scss
animation-delay($delay)
```

## Пример использования
```scss
.block {
  ...
  @include animation-delay(3s);
}
```

# `animation-direction()`
Миксин `animation-direction()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-direction` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-direction`).

> CSS-свойство `animation-direction `определяет, должна ли анимация воспроизводиться вперёд, назад или переменно вперёд и назад.
>
> [Подробнее на MDN →](https://developer.mozilla.org/ru/docs/Web/CSS/animation-direction)

## Синтаксис миксина
- `$direction` - одно из вожможных значений

```scss
animation-direction($direction)
```

### Возможные значения
- `normal` - анимация идёт с самого начала, после завершения цикла возвращается к исходному состоянию.
- `alternate` - анимация идёт с начала до конца, затем плавно возвращается в исходное положение.
- `reverse` - анимация идёт с конца цикла, после его завершения возвращается к исходному состоянию.
- `alternate-reverse` - анимация идёт с конца до начала, затем плавно возвращается в исходное положение.

## Пример использования
```scss
.block {
  ...
  @include animation-direction(normal);
}
```

# `animation-duration()`
Миксин `animation-duration()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-duration` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-duration`).

> Задаёт время в секундах или миллисекундах, сколько должен длиться один цикл анимации. По умолчанию значение равно `0s`, это означает, что никакой анимации нет.
>
> Можно указать несколько значений, перечисляя их через запятую. Отрицательные значения и значения без указания единиц времени (s или ms) недопустимы и будут игнорироваться.
>
> [Подробнее на WebRef →](https://webref.ru/css/animation-duration)

## Синтаксис миксина
- `$duration` - время длительности
```scss
animation-duration($duration)
```

## Пример использования
```scss
.block {
  ...
  @include animation-duration(1s);
}
```

# `animation-iteration-count()`
Миксин `animation-iteration-count()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-iteration-count` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-iteration-count`).

> Свойство определяет, сколько раз проигрывать цикл анимации до её остановки.
>
> [Подробнее на WebRef →](https://webref.ru/css/animation-iteration-count)

## Синтаксис миксина
- `$iteration-count` - одно из возможных значений
```scss
animation-iteration-count($iteration-count)
```

### Возможные значения
- `infinite` - анимация повторяется бесконечно.
- `<число>` - cколько раз должна повторяться анимация.

  > Отрицательные значения не допустимы. Можно использовать числа меньше единицы, для примера `0.5` будет означать половину цикла анимации.

## Пример использования
```scss
.block {
  ...
  @include animation-iteration-count(infinite);
}
```

# `animation-name()`
Миксин `animation-name()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-name` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-name`).

> Устанавливает одну или несколько анимаций, которые применяются к элементу. Представляет собой имя, связанное с правилом `@keyframes`, оно в свою очередь задаёт последовательность движения.
>
> [Подробнее на WebRef →](https://webref.ru/css/animation-name)

## Синтаксис миксина
- `$name` - одно из возможных значений
```scss
animation-name($name)
```

### Возможные значения
- `none` - отключает анимацию.
- `<идентификатор>` - текстовая строка, которая связана с анимацией.

  > Идентификатор должен начинаться с латинской буквы или подчёркивания (_), также может содержать цифры от 0 до 9 и дефис (-). Запрещено использовать зарезервированные ключевые слова `none`, `unset`, `inherit`, `initial`.

## Пример использования
```scss
.block {
  ...
  @include animation-name(myFrames);
}

@include keyframes(myFrames) { ... }
```

# `animation-play-state()`
Миксин `animation-play-state()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-play-state` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-play-state`).

> Свойство определяет, проигрывать анимацию или поставить её на паузу. При продолжении установленной на паузе анимации она начинается с того момента где была остановлена.
>
> [Подробнее на WebRef →](https://webref.ru/css/animation-play-state)

## Синтаксис миксина
- `$state` - одно из возможных значений
```scss
animation-play-state($state)
```

### Возможные значения
- `running` - проигрывать анимацию.
- `paused` - поставить анимацию на паузу.

## Пример использования
```scss
.block {
  ...
  @include animation-play-state(running);
}
```

# `animation-timing-function()`
Миксин `animation-timing-function()` также является лишь обёрткой над миксином `prefixer()`, который добавляет CSS-свойству `animation-timing-function` браузерные префиксы (в нашем случае префиксы прописаны в переменной `$prfxs_animation-timing-function`).

> Устанавливает, согласно какой функции времени должна происходить анимация каждого цикла между ключевыми кадрами. Она представляет собой математическую функцию, показывающую, как быстро по времени меняется значение свойства. Начальная точка имеет координаты 0.0, 0.0, конечная — 1.0, 1.0, при этом функция по оси ординат может превышать эти значения в большую или меньшую сторону (рис. ниже).
>
> ![Рис. 1](https://webref.ru/assets/images/css/css_timing-function-1.png)
>
> [Подробнее на WebRef →](https://webref.ru/css/animation-timing-function)

## Синтаксис миксина
- `$values...` - одно из возможных значений
```scss
animation-timing-function($values...)
```

### Возможные значения
- **`ease`** - анимация начинается медленно, затем ускоряется и к концу движения опять замедляется.

  ![](https://webref.ru/assets/images/css/css_timing-function-ease.png)

  > Аналогично `cubic-bezier(0.25,0.1,0.25,1)`.

- **`ease-in`** - анимация медленно начинается, к концу ускоряется.

  ![](https://webref.ru/assets/images/css/css_timing-function-ease-in.png)

  > Аналогично `cubic-bezier(0.42,0,1,1)`.

- **`ease-out`** - анимация начинается быстро, к концу замедляется.

  ![](https://webref.ru/assets/images/css/css_timing-function-ease-out.png)

  > Аналогично `cubic-bezier(0,0,0.58,1)`.

- **`ease-in-out`** - анимация начинается и заканчивается медленно.

  ![](https://webref.ru/assets/images/css/css_timing-function-ease-in-out.png)

  > Аналогично `cubic-bezier(0.42,0,0.58,1)`.

- **`linear`** - одинаковая скорость от начала и до конца.

  ![](https://webref.ru/assets/images/css/css_timing-function-linear.png)

- **`step-start`** - как таковой анимации нет.

  ![](https://webref.ru/assets/images/css/css_timing-function-step-start.png)
  > Стилевые свойства сразу же принимают конечное значение.

- **`step-end`** - как таковой анимации нет.

  ![](https://webref.ru/assets/images/css/css_timing-function-step-end.png)
  > Стилевые свойства находятся в начальном значении заданное время, затем сразу же принимают конечное значение.

- **`steps`** - ступенчатая функция, имеющая заданное число шагов.
`animation-timing-function: steps(<число>, start | end)`

  Здесь:
  - `<число>` - целое число больше нуля,
  - `start` - задаёт полунепрерывную снизу функцию,
  - `end` - задаёт [полунепрерывную сверху функцию](http://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%BB%D1%83%D0%BD%D0%B5%D0%BF%D1%80%D0%B5%D1%80%D1%8B%D0%B2%D0%BD%D0%B0%D1%8F_%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D1%8F).

  <br>

  ![](https://webref.ru/assets/images/css/css_timing-function-steps.png)

- **`cubic-bezier`** - задаёт функцию движения в виде [кривой Безье](http://ru.wikipedia.org/wiki/%D0%9A%D1%80%D0%B8%D0%B2%D0%B0%D1%8F_%D0%91%D0%B5%D0%B7%D1%8C%D0%B5).

## Пример использования
```scss
.block {
  ...
  @include animation-timing-function(linear);
}
```
