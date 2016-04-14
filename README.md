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
* http://gruntjs.com/ — Grunt.

## Синтаксический анализ и верификация стиля
* http://eslint.org/ — eslint. По умолчанию он ничего не делает, включайте правила группами или по одному. Стилистические правила настраиваются.
* https://github.com/babel/babel-eslint — Для поддержки async/await надо включить его, через `parser: babel-eslint`.

## Трансплиттер для поддержки фич ECMAScript 2015/2016/2017 на тех платформах, что их нативно не поддерживают
* https://babeljs.io/ — сам Babel. По умолчанию ничего не делает, включайте правила или группы правил.
* https://www.npmjs.com/package/babel-preset-es2015 — группа правил для поддержки ECMAScript 2015 везде (включая браузеры).
* https://www.npmjs.com/package/babel-preset-es2015-node4 — группа правил для поддержки ECMAScript 2015, при учёте что у вас версия Node.js не ниже 4.0.
* https://www.npmjs.com/package/babel-preset-es2015-node5 — группа правил для поддержки ECMAScript 2015, при учёте что у вас версия Node.js не ниже 5.0.
* https://www.npmjs.com/package/babel-preset-stage-3 — поддержка фич, находящихся в Stage 3 (кандидат в спецификацию), включая async/await.

На всякий случай: stage 3 — кандидат в спецификацию, stage 2 — черновик, stage 1 — предложение, stage 0 — поиграться.

## Тестирование
* http://chaijs.com/, http://mochajs.org/, https://github.com/jasmine/jasmine — библиотеки для построения тестов.
* https://github.com/karma-runner/karma — Karma, модульная обёртка для простой настройки тестов на стороне браузера. Само тестирование проводится например через Jasmine или Mocha (в зависимости от настроек).
* https://github.com/ariya/phantomjs/ — PhantomJS, Scriptable Headless WebKit.


* https://travis-ci.org/ — Travis CI. Выполняет автоматические тесты (указанные вами в `scripts.test`, просто запускает `npm test`) на каждый  пуш в мастер и на все пулл-реквесты.
 
 Не указывайте в конфиге трависа никакие ключи, указывайте их на сайте трависа в настройках, в безопасных переменных окружения — так они будут доступны только вашим веткам.
* https://github.com/gotwarlost/istanbul — Istanbul, анализирует покрытие кода тестами. На самом деле напрямую использовать обычно не надо, он интегрирован в системы тестирования.
* https://coveralls.io/, https://codecov.io/ — сервисы, которые принимают результат анализа покрытия, строят красивые графики, подсвечивают код и дают ссылку на бейдж с процентами покрытия (чтобы добавит в ридми). Можно настроить так, чтобы он браковал все пулл реквесты, которые снижают покрытие больше чем на сколько-то (или ниже порога).
 
 Сам анализ покрытия выполняется через istanbul на вашем CI (например, на Travis), и оттуда уже загружается на один из сервисов визуализации покрытия.

## Память и сборщик мусора
* https://github.com/bnoordhuis/node-heapdump — модуль для получения heapdump-ов. Они читаются хромом, но в его настройках надо включить «Show advanced heap snapshot properties» (см. https://github.com/bnoordhuis/node-heapdump/pull/80).
* http://jayconrod.com/posts/55/a-tour-of-v8-garbage-collection — общая схема работы сборщика мусора.
* gc() — mark-sweep, gc(true) — scavenge, но вручную из лучше не использовать, они не зря за флагом спрятаны.
* Если нужно ограничить использование памяти — используйте `--max_old_space_size` и другие ограничители, полный список по `node --v8-options`.

## Таблицы совместимости (статус разных фич в браузерах и Node.js)
* http://kangax.github.io/compat-table/es6/ — ECMAScript2015, там же есть вкладки для ES5 (прошлого) и next (возможно, будущего) стандарта.
* http://node.green/ — аналогичная таблица, но только для Node.js
* https://www.chromestatus.com/features — статус разных фич в Chrome и v8. Chrome 50 — v8 5.0, Chrome 46 — v8 4.6, и по аналогии (достаточно далеко вниз). Тут можно посмотреть, что планируется в какой версии движка v8.

## Оптимизация
* https://github.com/petkaantonov/bluebird/wiki/Optimization-killers — как делать не надо. Тут некоторые данные устарели и нуждаются в обновлении, что-то из этого уже оптимизировано в режиме 'use strict'. Но всё равно следует ознакомиться.
* … (будет дополнено)
