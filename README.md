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
* https://nodejs.org/api/process.html#process_event_unhandledrejection — сигнал о необработанной ошибке в Promise.
* http://www.ecma-international.org/ecma-262/6.0/ — спецификация ECMAScript 2015.

--

Дальше группировка по темам, а не по номерам занятий.

--

## ECMAScript 2017

* https://tc39.github.io/ecmascript-asyncawait/ — async/await.

## Сборка и выполнение задач
* http://gulpjs.com/ — Gulp. Мы рассматривали его.
* http://gruntjs.com/ — Grunt

## Синтаксический анализ и верификация стиля
* http://eslint.org/ — eslint. По умолчанию он ничего не делает, включайте правила группами или по одному. Стилистические правила настраиваются.
* https://github.com/babel/babel-eslint — Для поддержки async/await надо включить его через `parser: babel-eslint`.

## Трансплиттер для поддержки фич ECMAScript 2015/2016/2017 на тех платформах, что их нативно не поддерживают
* https://babeljs.io/ — сам Babel. По умолчанию ничего не делает, включайте правила или группы правил.
* https://www.npmjs.com/package/babel-preset-es2015 — группа правил для поддержки ECMAScript 2015 везде (включая браузеры).
* https://www.npmjs.com/package/babel-preset-es2015-node4 — группа правил для поддержки ECMAScript 2015, при учёте что у вас версия Node.js не ниже 4.0.
* https://www.npmjs.com/package/babel-preset-es2015-node5 — группа правил для поддержки ECMAScript 2015, при учёте что у вас версия Node.js не ниже 5.0.
* https://www.npmjs.com/package/babel-preset-stage-3 — поддержка фич, находящихся в Stage 3 (кандидат в спецификацию), включая async/await.

На всякий случай: stage 3 — кандидат в спецификацию, stage 2 — черновик, stage 1 — предложение, stage 0 — поиграться.
