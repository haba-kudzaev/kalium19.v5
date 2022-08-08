<img title="Логотип проекта" src="https://github.com/rx1310/kalium19/blob/main/.github/logo.png?raw=true" alt="Logo" width="80px" align="right" /> Kalium19
======
:package: Набор утилит, миксинов, расширений на языке препроцессора [Sass](https://github.com/sass) для помощи в ускорении и упрощении написания CSS-стилей.

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/rx1310/kalium19/npm%20publisher?label=npm%20publisher&style=flat-square)](https://npmjs.com/package/@rx1310/kalium19)
[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/rx1310/kalium19/GitHub%20Packages%20publisher?label=github%20package%20publisher&style=flat-square)](https://github.com/rx1310/kalium19/packages/1547304)

![GitHub](https://img.shields.io/github/license/rx1310/kalium19?style=flat-square)
![GitHub language count](https://img.shields.io/github/languages/count/rx1310/kalium19?style=flat-square)
![GitHub top language](https://img.shields.io/github/languages/top/rx1310/kalium19?style=flat-square)
![npm](https://img.shields.io/npm/v/@rx1310/kalium19?label=npm%3A%20version&style=flat-square)
![npms.io (popularity)](https://img.shields.io/npms-io/popularity-score/@rx1310/kalium19?label=npm%3A%20popularity&style=flat-square)
![Libraries.io dependency status for latest release, scoped npm package](https://img.shields.io/librariesio/release/npm/@rx1310/kalium19?label=npm%3A%20dependencies&style=flat-square)
![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@rx1310/kalium19?label=npm%3A%20minified%20size&style=flat-square)
![npm](https://img.shields.io/npm/dm/@rx1310/kalium19?label=npm%3A%20downloads&style=flat-square)
![npm (prod) dependency version](https://img.shields.io/npm/dependency-version/@rx1310/kalium19/sass?style=flat-square)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/rx1310/kalium19?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/rx1310/kalium19?style=flat-square)
![GitHub contributors](https://img.shields.io/github/contributors/rx1310/kalium19?style=flat-square)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/rx1310/kalium19?style=flat-square)
![GitHub repo size](https://img.shields.io/github/repo-size/rx1310/kalium19?style=flat-square)
![GitHub issues](https://img.shields.io/github/issues/rx1310/kalium19?style=flat-square)
![GitHub closed issues](https://img.shields.io/github/issues-closed/rx1310/kalium19?style=flat-square)
![GitHub pull requests](https://img.shields.io/github/issues-pr/rx1310/kalium19?style=flat-square)
![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/rx1310/kalium19?style=flat-square)
![GitHub milestones](https://img.shields.io/github/milestones/all/rx1310/kalium19?style=flat-square)
[![Поддержка Dart Sass](https://img.shields.io/badge/Dart%20Sass%20-1.23.0%2B-cc6699?style=flat-square)](https://shields.io/)
[![Поддержка LibSass](https://img.shields.io/badge/LibSass-⤬-red?style=flat-square)](https://shields.io/)
[![Поддержка ruby-sass](https://img.shields.io/badge/Ruby%20Sass%20-⤬-red?style=flat-square)](https://shields.io/)
[![Поддержка node-sass](https://img.shields.io/badge/node--sass%20-⤬-red?style=flat-square)](https://shields.io/)

## Установка и использование
Для начала необходимо иметь установленный пакетный менеджер (напр.: [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) или любой другой совместимый). Я буду показывать на примере npm.

Порядок действий:

1. откройте терминал (командную строку) в папке проекта:

    ```bash
    cd my-project
    ```

2. введите команду для установки npm-пакета [`@rx1310/kalium19`](https://npmjs.com/package/@rx1310/kalium19) (также есть на [GitHub Packages](https://github.com/rx1310/kalium19/packages/1547304)) в проект:

    ```bash
    npm install @rx1310/kalium19
    ```

3. дождитесь установки всех пакетов и зависимостей в проект
4. в основной Sass-файл стилей пропишите импорт модуля `kalium19`:

    ```scss
    @use 'node_modules/@rx1310/kalium19' as *;
    ```

    > `*` означает, что миксины и функции из пакета `@rx1310/kalium19` доступны глобально. Вы можете использовать [пространство имён в Sass](https://sass-lang.com/documentation/at-rules/use#choosing-a-namespace), чтобы избежать возможных конфликтов с другими пакетами/библиотеками.

5. для проверки правильного импорта можно вставить `@include check;` в файл стилей после импорта:

    ```scss
    @use 'node_modules/@rx1310/kalium19' as *;

    @include check;
    ```
    и в консоли получить след. сообщение:

    ```log
    index.scss:3 Debug: Installed Kalium19 v4.1.0
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

6. готово!

### А если не используется пакетный менеджер?
В таком случае можно просто склонировать репозиторий проекта в папку проекта, используя [Git](https://git-scm.com/downloads):

```bash
git clone https://github.com/rx1310/kalium19
```

> Импорт Kalium19 производится также, как и в пункте 4 в варианте с пакетным менеджером.

Также можно склонировать Kalium19 в качестве субмодуля Git:

```bash
git submodule add https://github.com/rx1310/kalium19
```

### А если не установлена утилита Git?
Это, конечно же, странно, но возможно. В таком случае можно просто скачать архив [репозитория с GitHub](https://github.com/rx1310/kalium19/releases):

1. выберите версию
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

## Документация
На данный момент документация формируется средствами утилиты [sassdoc](http://sassdoc.com/) и доступна по [этой ссылке](https://rx1310.github.io/kalium19).

## Лицензия
Проект [Kalium19](https://github.com/rx1310/kalium19) распространяется совершенно бесплатно и находится под защитой лицензии [MIT](LICENSE).

Инструментарий, используемый в разработке, распространяется по указанной автором / компанией / разработчиком лицензии, не зависящей от этого проекта!

```
MIT License
Copyright (c) 2022, Haba Kudzaev (rx1310) <rx1310@inbox.ru>
```

> Если Вы нашли нарушение чьей-либо лицензии в моем проекте, то просьба написать мне → [Telegram](https://t.me/rx1310), [эл. почта](mailto:rx1310@inbox.ru) или [VK](https://vk.com).
