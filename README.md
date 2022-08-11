[![Поддержка Dart Sass](https://img.shields.io/badge/dart--sass%20-1.23.0%2B-cc6699)](https://shields.io/)
[![Поддержка LibSass](https://img.shields.io/badge/libsass-⤬-d50000)](https://shields.io/)
[![Поддержка ruby-sass](https://img.shields.io/badge/ruby--sass%20-⤬-d50000)](https://shields.io/)
[![Поддержка node-sass](https://img.shields.io/badge/node--sass%20-⤬-d50000)](https://shields.io/)

# Kalium19 ![npm](https://img.shields.io/npm/v/@rx1310/kalium19?color=fbd2e0&label=%20)

<img title="Логотип проекта" src="https://github.com/rx1310/kalium19/blob/develop/.github/logo_rounded.png?raw=true" alt="Логотип проекта Kalium19 от Асхаба Кудзаева" width="90px" align="right" />

:package: Большой набор миксинов, карт и функций на языке препроцессора [Sass](https://github.com/sass) для помощи в ускорении и упрощении написания CSS-стилей.

[![Статус публикации пакета на GitHub Packages через Action](https://img.shields.io/github/workflow/status/rx1310/kalium19/GitHub%20Packages%20publisher?label=github%20packages&logo=github)](https://github.com/rx1310/kalium19/packages/1547304)
[![Статус публикации пакета на npm через GitHub Action](https://img.shields.io/github/workflow/status/rx1310/kalium19/npm%20publisher?label=npm&logo=npm)](https://npmjs.com/package/@rx1310/kalium19)

![npm (prod) dependency version](https://img.shields.io/npm/dependency-version/@rx1310/kalium19/sass?logo=sass&logoColor=fff&color=fff)
![GitHub top language](https://img.shields.io/github/languages/top/rx1310/kalium19?color=%23c76394)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/rx1310/kalium19?color=fbd2e0)
![GitHub repo file count](https://img.shields.io/github/directory-file-count/rx1310/kalium19?label=files%20%22.%2F%22)
![GitHub repo file count (custom path)](https://img.shields.io/github/directory-file-count/rx1310/kalium19/modules?label=files%20%22modules%2F%22)
![GitHub repo size](https://img.shields.io/github/repo-size/rx1310/kalium19?color=fbd2e0)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/rx1310/kalium19?color=fbd2e0)
![GitHub Release Date](https://img.shields.io/github/release-date/rx1310/kalium19?color=fff)
![GitHub closed issues](https://img.shields.io/github/issues-closed/rx1310/kalium19?color=4caf50&logo=github)
![GitHub issues](https://img.shields.io/github/issues/rx1310/kalium19?color=e91e63&logo=github)
![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/rx1310/kalium19?color=4caf50&logo=github)
![GitHub pull requests](https://img.shields.io/github/issues-pr/rx1310/kalium19?color=009688&logo=github)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rx1310/kalium19?color=c5e1a5&logo=github)
![GitHub contributors](https://img.shields.io/github/contributors/rx1310/kalium19?color=c51162&logo=github)
![GitHub last commit](https://img.shields.io/github/last-commit/rx1310/kalium19?color=66bb6a&logo=github)
![npm downloads](https://img.shields.io/npm/dm/@rx1310/kalium19?label=downloads&logo=npm)
![npms.io (quality)](https://img.shields.io/npms-io/quality-score/@rx1310/kalium19?label=quality&logo=npm)
![npms.io (popularity)](https://img.shields.io/npms-io/popularity-score/@rx1310/kalium19?label=popularity&logo=npm)
![npms.io (maintenance)](https://img.shields.io/npms-io/maintenance-score/@rx1310/kalium19?label=maintenance&logo=npm)
![npms.io (final-score)](https://img.shields.io/npms-io/final-score/@rx1310/kalium19?label=score&logo=npm)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/@rx1310/kalium19?label=gzip%20size&logo=npm)
![License](https://img.shields.io/github/license/rx1310/kalium19?color=3da13b)

## Приступая к работе...
Для начала необходимо удостовериться, что в вашем проекте (в котором будет использоваться Kalium19) установлена npm-зависимость [sass](https://www.npmjs.com/package/sass), т.к. Kalium19 сам ничего не компилирует, а лишь является набором готовых стилей и функций на языке препроцессора Sass.

> Предпологается, что с языком Sass (SCSS) вы уже знакомы и о необходимости установленного NodeJS и npm вам известно.

### Установка
Установка Kalium19 не отличается ничем от других npm-пакетов.

Порядок действий:

1. перейдите в корень проекта через терминал (Windows-like: командную строку):

    ```bash
    cd my-project
    ```

2. введите команду для установки npm-пакета [`@rx1310/kalium19`](https://npmjs.com/package/@rx1310/kalium19) (также есть на [GitHub Packages](https://github.com/rx1310/kalium19/packages/1547304)) в проект:

    ```bash
    npm install @rx1310/kalium19
    ```

    > Если Sass не установлен в проект:
    > ```bash
    > npm install sass --save-dev
    > ```

3. дождитесь установки всех пакетов и зависимостей в проект и в основной Sass-файл стилей пропишите импорт модуля `kalium19`:

    ```scss
    @use 'node_modules/@rx1310/kalium19' as *;
    ```

    `*` означает, что миксины и функции из пакета `@rx1310/kalium19` доступны глобально. Вы можете использовать [пространство имён в Sass](https://sass-lang.com/documentation/at-rules/use#choosing-a-namespace), чтобы избежать возможных конфликтов с другими пакетами/библиотеками.

    > Именно из-за использования модульной системы Sass Kalium19 лишается поддержки старых компиляторов (LibSass, например), т.к. они не поддерживают (или поддерживают плохо) работу с директивами `@use` и `@forward`.


4. для проверки правильного импорта можно использовать миксин `@include check;` в файле стилей после импорта:

    ```scss
    @use 'node_modules/@rx1310/kalium19' as *;

    @include check;
    ```
    и в консоли получить след. сообщение:

    ```log
    index.scss:3 Debug: Installed Kalium19!
    ```

    а в итоговом CSS-файле должно быть что-то похожее:

    ```css
    /*
      * @name    : @rx1310/kalium19 (title: Kalium19)
      * @license : MIT
      * @author  : Haba Kudzaev (rx1310) <rx1310@inbox.ru>
      * @homepage: https://github.com/rx1310/kalium19
      */
    ```

5. готово!

#### А если не используется пакетный менеджер?
В таком случае можно просто склонировать репозиторий проекта в папку проекта, используя [Git](https://git-scm.com/downloads):

```bash
git clone https://github.com/rx1310/kalium19
```

> Импорт Kalium19 производится также, как и в пункте 4 в варианте с пакетным менеджером, но путь до пакета указывается другой.

Также можно склонировать Kalium19 в качестве субмодуля Git:

```bash
git submodule add https://github.com/rx1310/kalium19
```

#### А если не установлена утилита Git?
В таком случае можно просто скачать архив [репозитория с GitHub](https://github.com/rx1310/kalium19/releases):

1. выберите версию (последняя версия ![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/rx1310/kalium19?label=%20&color=000&logo=github))
2. на странице релиза версии внизу выберите ссылку [Source code (zip)](https://github.com/rx1310/kalium19/releases) и скачайте архив нужной версии проекта.

> Если у Вас установлен [curl](https://curl.se/) или [Wget](https://www.gnu.org/software/wget/), то можете воспользоваться командой в терминале:
> ```bash
> # curl
> curl -L -O https://github.com/rx1310/kalium19/archive/refs/heads/main.zip
>
> # wget
> wget --no-check-certificate --content-disposition https://github.com/rx1310/kalium19/archive/refs/heads/main.zip
> ```
> Данные команды скачают архив версии с ветки [`main`](https://github.com/rx1310/kalium19/tree/main).

## Настройка Kalium19
После подключения Kalium19 можно сразу же прописать параметры для пакета. Например, подключим Kalium19 и настроим отображение ошибок в режиме «Предупредительный» (warn), а также отключим генерацию свойства `opacity` для браузера Internet Explorer 5 и еще отключим префиксы правила `@keyframes` для одного старого браузера от Microsoft (RIP) и Opera на старом движке (новую версию на Chromium это не коснется):

```scss
// SCSS Input:
@use '../kalium19' as k19 with (
	$strict-mode: warn,
	$opacity: (
		ie5: false,
		ie8: true
	),
	$keyframes: (
		webkit: true,
		moz: true,
		ms: false,
		o: false
	)
);

.block {
	@include k19.animation-direction(reverse);
	@include k19.opacity(.7);
	@include k19.animation(animPulse 5s infinite)
}

@include k19.keyframes(animPulse) {
	0%   { background-color: #001F3F; }
	100% { background-color: #FF4136; }
}
```
```css
/* CSS Output: */
.block {
	-webkit-animation-direction: reverse;
	-moz-animation-direction: reverse;
	-o-animation-direction: reverse;
	animation-direction: reverse;
	-moz-opacity: 0.7;
	-khtml-opacity: 0.7;
	opacity: 0.7;
	/* for IE 8 */
	-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=70)";
	-webkit-animation: animPulse 5s infinite;
	-moz-animation: animPulse 5s infinite;
	-o-animation: animPulse 5s infinite;
	animation: animPulse 5s infinite;
}

@-webkit-keyframes animPulse {
	0%   { background-color: #001F3F; }
	100% { background-color: #FF4136; }
}
@-moz-keyframes animPulse {
	0%   { background-color: #001F3F; }
	100% { background-color: #FF4136; }
}
@keyframes animPulse {
	0%   { background-color: #001F3F; }
	100% { background-color: #FF4136; }
}
```

Все указанные настройки были учтены и миксины отработали с учетом этих самых настроект. Весь список изменяемых настроект находится в файле [config.scss](modules/_config.scss).

## Директива `@import`
Если Вы до сих пор используете директиву `@import` в Sass, то вот что говорят разработчики Sass в своем блоге:

> The Sass team wants to allow for a large amount of time when `@use` and `@import` can coexist, to help the ecosystem smoothly migrate to the new system. However, doing away with `@import` entirely is the ultimate goal for simplicity, performance, and CSS compatibility.
> <details><summary>Перевод (машинный)</summary><br><p>Команда Sass хочет предусмотреть большое количество времени, когда <code>@use</code>  и <code>@import</code> могут сосуществовать, чтобы помочь экосистеме плавно перейти на новую систему. Однако полный отказ от <code>@import</code> является конечной целью для простоты, производительности и совместимости с CSS.</p></details>

Да, если вы не желаете использовать модульную систему в Sass, то импорт Kalium19 миксинов, переменных и функций сохранена, до полного прекращения поддержки в Sass.

На примере ниже мы импортируем библиотеку "по-старому" через директиву `@import` и функциональность по сути не нарушена.
```scss
// SCSS Input
@import '../kalium19';

$prfxs_border-radius: webkit moz; // выбираем нужные префиксы

.block {
	@include wh(42px);
	@include border-radius(12px); // префиксы подставляются к свойству
}
```
```css
/* CSS Output */
.block {
	width: 42px;
	height: 42px;
	-webkit-border-radius: 12px; /* свойство генерируется с префиксом для браузера */
	-moz-border-radius: 12px; /* свойство генерируется с префиксом для браузера */
	border-radius: 12px;
}
```

## Лицензия
Проект [Kalium19](https://github.com/rx1310/kalium19) распространяется совершенно бесплатно и находится под защитой лицензии [MIT](LICENSE).

Инструментарий, используемый в разработке, распространяется по указанной автором / компанией / разработчиком лицензии, не зависящей от этого проекта!

```
MIT License

Copyright (c) 2022, Haba Kudzaev (rx1310) <rx1310@inbox.ru>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

> Если Вы нашли нарушение чьей-либо лицензии в моем проекте, то просьба написать мне → [Telegram](https://t.me/rx1310), [эл. почта](mailto:rx1310@inbox.ru) или [VK](https://vk.com).

![GitHub watchers](https://img.shields.io/github/watchers/rx1310/kalium19?style=social)
![GitHub Repo stars](https://img.shields.io/github/stars/rx1310/kalium19?style=social)
![GitHub forks](https://img.shields.io/github/forks/rx1310/kalium19?style=social)
