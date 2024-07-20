![Image](/assets/poster.webp)

С помощью этого скрипта [IMDB](https://www.imdb.com/), [TMDB](https://www.themoviedb.org/), [Kinopoisk](https://www.kinopoisk.ru/) и [Letterboxd](https://letterboxd.com/) станут бесплатными онлайн-кинотеатрами! На каждой странице с фильмом или сериалом в левом верхнем углу появится флажок. Нажав на него, вы откроете плеер с фильмом.

**RUS** | [ENG](README.eng.md)

<br>

## Установка 🎓

1. Установите одно из расширений для запуска пользовательских скриптов:

    - [Tampermonkey](https://www.tampermonkey.net/) _(рекомендуемое)_
    - [Violentmonkey](https://violentmonkey.github.io/)
    - [Greasemonkey](https://www.greasespot.net/)
    - [Userscripts](https://github.com/quoid/userscripts)

2. Включите [режим разработчика в вашем браузере](https://www.tampermonkey.net/faq.php?locale=ru#Q209).
3. Установите скрипт, перейдя по [этой ссылке](https://github.com/Kirlovon/Tape-Operator/raw/master/userscript/tape-operator.user.js). _(либо скачайте `tape-operator.user.js` и установите вручную)_

Готово, теперь откройте страницу с фильмом _([пример](https://letterboxd.com/film/babylon-2022/))_ и нажмите на флажок в левом верхнем углу!

> Если флажок не появляется, проверьте, установлен ли скрипт правильно, и перезапустите браузер.

<br>

## Deploy 🚀

На случай, если ссылка на плеер будет заблокирована в вашей стране, вы можете самостоятельно развернуть свою собственную версию сайта!

> Эта инструкция предназначена для разработчиков и других пользователей с необходимыми техническими навыками.

1. Опубликуйте статический сайт, находящийся в папке `player` этого репозитория.

    - Файлы и страница `index.html` должны быть доступна по основному адресу. _(http://example.com/index.html или просто http://example.com)_

    - Удалите скрипт для аналитики, находящийся в заголовке файла `index.html`, чтобы не отправлять анонимную аналитику.

2. Отредактируйте скрипт из папки `userscript`:

    - Замените переменную `PLAYER_URL` на ссылку на ваш сайт.

    - Добавьте строку с ссылкой на ваш сайт в заголовке `@match`. Это необходимо, чтобы браузер выполнял скрипт на вашей странице с плеером.

    - Удалите из файла заголовки `@updateURL` и `@downloadURL`, чтобы скрипт не пытался обновить себя.

    - Убедитесь, что версия в заголовке `@version` равна или не ниже версии, указанной в файле `player.js`, в переменной `REQUIRED_VERSION`. Иначе, на сайте будет уведомление об устаревшем скрипте.

3. Установите отредактированный скрипт.

> Самостоятельный хостинг не гарантирует 100% работу сайта, так как для получения источников используется [Kinobox API](https://kinobox.tv/), который пока что невозможно самостоятельно развернуть.

<br>

## Отказ от Ответственности

Плеер работает на основе [Kinobox API](https://kinobox.tv/), и предоставляется исключительно в ознакомительных целях!

Проект не хранит и не распространяет пиратский контент. Все права на материалы принадлежат их законным владельцам. Для удаления незаконного контента обращайтесь к первоисточнику. Я не несу ответственности за содержание, размещенное на сторонних ресурсах.

**_Пиратство - плохо!_**

<br>

## Лицензия

MIT _([LICENSE](https://github.com/Kirlovon/Tape-Operator/blob/master/LICENSE) файл)_
