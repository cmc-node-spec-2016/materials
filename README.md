# Материалы

Большая часть ссылок на английском.
Тут перечислено не всё, но основное.

## Первое занятие

#### Вводная информация
* https://nodejs.org/ — официальный сайт.
* https://nodejs.org/en/about/ — совсем краткое описание концепции.
* https://npmjs.org/ — репозиторий пакетов и пакетный менеджер.
* https://github.com/nodejs/node — Node.js на GitHub (исходники, задачи).
* Картинки для иллюстрации асинхронного ввода-вывода с циклом событий.
* http://www.modulecounts.com/ — данные по количеству модулей.

#### Документация
* https://nodejs.org/dist/latest-v5.x/docs/api/ — API Node.js
* https://developer.mozilla.org/en/docs/Web/JavaScript — удобная документация по JavaScript.

#### Установка

* https://nodejs.org/en/download/ — официальные сборки (в архивах).
* https://github.com/nodesource/distributions — репозитории для Debian, RedHat, Ubuntu, CentOS, Fedora.
* https://nvm.sh/ — менеджер версий официальных сборок.

Устанавливаем последнюю стабильную версию 5.x.

## Второе занятие

#### learnyounode

* https://www.npmjs.com/package/learnyounode
* https://github.com/workshopper/learnyounode

Установка была не в глобальную папку (т.е. без `-g`), а в пустую директорию с последующим обновлением `PATH`, симлинком в `~/.bin/`, или запуском `./node_modules/.bin/learnyounode` руками — чтобы не засорять систему глобальной установкой. В принципе, это по желанию. С `nvm` даже с `-g` установка происходит не в глобальную папку, а в каталог nvm.

## Третье занятие

* Область видимости переменных.
* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/let — let.
* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/const — const.
* http://jsrocks.org/2015/01/temporal-dead-zone-tdz-demystified/ — примеры c TDZ.
* https://bugzilla.mozilla.org/show_bug.cgi?id=1069480 — неточности работы SpiderMonkey (JS движка Firefox) с TDZ, ещё несколько примеров.
* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Generator — генераторы.
* https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Promise — Promise.
* https://www.npmjs.com/package/bluebird — Bluebird, быстрая реализация Promise (плюс дополнительные фичи вроде promisify, который строит API на Promise из API на nodebacks).
* http://www.ecma-international.org/ecma-262/6.0/ — спецификация ECMAScript 2015.
