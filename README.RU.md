![alt text](https://raw.githubusercontent.com/gongled/cartomatic/master/cartomatic.png "Cartomatic Logo")

## О проекте

Cartomatic поможет настроить вам сервер под CS-Cart и Multi-Vendor 4.0+.

## Быстрая установка

Войдите на сервер по SSH и выполните команду под суперпользователем (root):

    curl -sL http://cartoma.tk/installer | bash -s -- yourdomain.ltd

Если не установлен cURL:

    wget -qO - http://cartoma.tk/installer | bash -s -- yourdomain.ltd

Готово. Сервер настроен.

## Обычная установка

Войдите на сервер по SSH и выполните команду под суперпользователем (root):

    curl -sL http://cartoma.tk/preconf | bash

Перейдите в каталог с настройками и отредактируйте JSON-конфиг:

    cd /srv/cartomatic/<version>
    vim config/simple.json

Дополнительно можете указать настройки сервисов в файлах каталога 'group_vars'.

Выполните настройку:

    ansible-playbook lamp.yml -c local -e @config/simple.json

Автоматически сгенерированные пароли будут сохранены в каталог 'credentials'.

## Поддерживаемые ОС

* Ubuntu 14.04 x86_64
* Ubuntu 14.10 x86_64
* Ubuntu 15.04 x86_64
* Debian 6 Squeeze x86_64
* Debian 7 Wheezy x86_64
* Debian 8 Jessie x86_64
* CentOS 6 x86_64
* CentOS 7 x86_64

## Ограничения

* Хорошо работает только на чистых инсталляциях.
* Нет совместимости с ISPManager, cPanel, Plesk и пр.

## Благодарности

* [@jsjant](https://github.com/jsjant) за название проекта.
* Воронину Андрею за дизайн логотипа.
* Дурновой Татьяне за помощь с переводом.

## Лицензия

GNU Public Licence 3 (GPL v3)
