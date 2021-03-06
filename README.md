# Конфиг для Gulp

Краткое описание, подробное будет позже.


## Файлы

* `.gitignore` - образцовый gitignore. В начале файла необходимо вписать правильную целевую папку
* `package.json` - "список инструкций по установке" для `npm`
* `gulp-config.json` - конфигурация
* `gulpfile.js` - ядро


## Возможности

* Обработка CSS, Less, JS (ES6)
* Копирование остальных файлов без обработки
* Минификация CSS, Less, JS
* Обработка "на ходу" (без перезапуска `gulp`)
* Очистка целевой папки перед сборкой
* Игнорирование файлов в целевой папке (`cleanIgnore`)


### CSS

* Автопрефиксер (`gulp-autoprefixer` с параметрами: `last 2 versions`)
* Минификатор (`gulp-cssnano`)


### Less

* Компилятор в CSS (`gulp-less`)
* Автопрефиксер (`gulp-autoprefixer` с параметрами: `last 2 versions`)
* Минификатор (`gulp-cssnano`)


### JavaScript

* ES6 (`babel` c компилятором `es2015-without-strict`)
* Минификатор (`gulp-uglify`)

Babel некорректо обрабатывает некоторые плагины, из-за чего они перестают работать. Необходимо добавить их в игнор.


## Команды

* `npm install` - установка
* `npm update` - обновить пакет
* `npm install -g gulp` - установка `gulp`
* `gulp` - билд проекта с очисткой целевой папки
* `gulp watch` - билд проекта с очисткой целевой папки и отслеживание изменений
* `gulp --release` - билд проекта с очисткой целевой папки и минификацией