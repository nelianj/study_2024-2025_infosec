---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе 6
subtitle: Основы информационной безопасности
author:
  - Нджову Н.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 01 мая 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

## Цель работы

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1. Проверить работу SELinux на практике совместно с веб-сервером Apache.

## Выполнение лабораторной работы

Я вошла в свою учетную запись и убедилась, что SELinux работает в режиме принудительного применения целевой политики, используя команды getenforce и status(рис.1)

![проверка режима работы SELinux](image/Untitled1.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я запускаю сервер apache, затем использую браузер для доступа к веб-серверу, запущенному на компьютере, он запущен, как видно из вывода команды service httpd status(рис.2)

![Проверка работы Apache](image/Untitled2.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я нашла веб-сервер Apache в списке процессов, используя команду ps aux | grep httpd. Его контекст безопасности - http_t(рис.3)

![Контекст безопасности Apache](image/Untitled3.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я просмотрела текущее состояние коммутаторов SELinux для Apache, используя команду status -grep httpd(рис.4)

![Состояние переключателей SELinux](image/Untitled4.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я просмотрела статистику по политике, используя команду setinfo. Всего 8 пользователей, 39 ролей и 5135 типов(рис.5)

![Cтатистика по политике](image/Untitled5.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Типы подкаталогов, расположенных в каталоге /var/www с помощью команды ls - lZ /var/www, следующие: владельцем является root, только у владельца есть права на изменение. В каталоге нет файлов(рис.6)

![Типы поддиректорий](image/Untitled6.png){#fig:001 width=70%}

## Выполнение лабораторной работы

В директории /var/www/html нет файлов(рис.7)

![Типы файлов](image/Untitled7.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Только суперпользователь может создать файл, поэтому я создала файл с помощью команды touch.html и ввела в него код(рис.8 и рис.9)

![Создание файла](image/Untitled9.png){#fig:001 width=70%}

## Выполнение лабораторной работы

![Содержание файла](image/Untitled8.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я проверяю контекст созданного файла. По умолчанию это httpd_sys_content_type(рис.10)

![Контекст файла](image/Untitled10.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я получаю доступ к файлу через веб-сервер, вводя адрес в браузере http://127.0.0.1/test.html . Файл был успешно отображен(рис.11)

![Отображение файла](image/Untitled11.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я изучила справку man по httpd-selinux(рис.12)

![Изучение справки по команде](image/Untitled12.png){#fig:001 width=70%}

## Выполнение лабораторной работы

I change the context of the file /var/www/html/test.html from httpd_sys_content_t to any other that the httpd process should not have access to, for example, to samba_share_t: chcon -t samba_share_t /var/www/html/test.html css/var/www/html/test.html The context has really changed(рис.13)

![Изменение контекста](image/Untitled13.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Когда я пытаюсь отобразить файл в браузере, мы получаем сообщение об ошибке(рис.14)

![Отображение файла](image/Untitled14.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я просматриваю файлы журнала веб-сервера Apache и файл системного журнала: tail /var/log/messages. Если в системе запущены процессы setroubleshootd и audit, вы также можете увидеть ошибки, аналогичные перечисленным выше, в файле /var/log/audit/audit.log(рис.15)

![Попытка прочесть лог-файл](image/Untitled16.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Чтобы запустить веб-сервер Apache, прослушивающий TCP-порт 81, я открываю файл /etc/httpd/httpd.conf для внесения изменений(рис.16)

![Изменение файла](image/Untitled18.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Нахожу строчку Listen 80 и заменяю её на Listen 81(рис.17)

![Изменение порта](image/Untitled19.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я перезапускаю веб-сервер Apache. Сбой произошел из-за того, что порт 80 предназначен для локальной сети, а порт 81 - нет(рис.18)

![Попытка прослушивания другого порта](image/Untitled19a.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Проанализируйте лог-файлы: tail -nl /var/log/messages(рис.19)

![Проверка лог-файлов](image/Untitled20.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я просматриваю файлы /var/log/http/error_log, /var/log/httpd access_log и /var/log/audit/аудит.лог и выясняю, в каких файлах появились записи. Запись появилась в файле error_log(рис.20)

![Проверка лог-файлов](image/Untitled21.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я запускаю команду semanage port -at http_port_to tcp 81, после чего проверяю список портов командой semanage port -l | grep http_port_t Порт 81 появился в списке(рис.21)

![Проверка портов](image/Untitled22.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Перезапускаю сервер Apache(рис.22)

![Перезапуск сервера](image/Untitled23.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Теперь он работает, ведь мы внесли порт 81 в список портов httpd_port_t(рис.23)

![Проверка сервера](image/Untitled24.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Возвращаю в файле /etc/httpd/httpd.conf порт 80, вместо 81. Проверяю, что порт 81 удален, это правда(рис.24)

![Проверка порта 81](image/Untitled26.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Далее удаляю файл test.html, проверяю, что он удален(рис.25)

![Удаление файла](image/Untitled7.png){#fig:001 width=70%}

## Выводы

В ходе выполнения данной лабораторной работы были развиты навыки администрирования ОС Linux, получено первое практическое знакомство с технологией SELinux и проверена работа SELinux на практике совместно с веб-сервером Apache
