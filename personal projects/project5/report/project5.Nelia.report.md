---
## Front matter
title: "Отчет по идивидуальнной проекте 5"
subtitle: "Основы информационной безопасности"
author: "Нджову Нелиа"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Научиться использовать Burp Suite.

# Теоретическое введение

Burp Suite представляет собой набор мощных инструментов безопасности веб-приложений, которые демонстрируют реальные возможности злоумышленника, проникающего в веб-приложения. Эти инструменты позволяют сканировать, анализировать и использовать веб-приложения с помощью ручных и автоматических методов. Интеграция интерфейсов этих инструментов обеспечивает полную платформу атаки для обмена информацией между одним или несколькими инструментами, что делает Burp Suite очень эффективной и простой в использовании платформой для атаки веб-приложений.

# Выполнение лабораторной работы

Я запускаю локальный сервер, на котором открою веб-приложение DVWA для тестирования инструмента Burp Suite(рис.1).

![Запуск локального сервера](image/Untitled1.png){#fig:001 width=70%}

Я запускаю инструмент Burp Suite. После этого я открываю сетевые настройки браузера, для подготовке к работе(рис.2).

![Сетевые настройки браузера](image/Untitled2.png){#fig:002 width=70%}

Я изменяю настройки сервера для работы с proxy и захватом данных с помощью Burp Suite(рис.3)

![Настройки сервера](image/Untitled3.png){#fig:003 width=70%}

Я изменяю настройки Proxy инструмента Burp Suite для дальнейшей работы(рис.4).

![Настройки Burp Suite](image/Untitled4.png){#fig:004 width=70%}

Во вкладке Proxy устанавливаю "Intercept is on"(рис.5).

![Настройки Proxy](image/Untitled5.png){#fig:005 width=70%}

Чтобы Burp Suite исправно работал с локальным сервером, наобходимо установить параметр `network_allow_hijacking_loacalhost` на `true`(рис.6).

![Настройки параметров](image/Untitled6.png){#fig:006 width=70%}

Я пытаюсь зайти в браузере на DVWA, тут же во вкладки Proxy появляется захваченный запрос. Нажимаем "Forward", чтобы загрузить страницу(рис.7 и рис.8).

![Получаемые запросы сервера](image/Untitled8.png){#fig:007 width=70%}

![Получаемые запросы сервера](image/Untitled7.png){#fig:008 width=70%}

Загрузилась страница авторизации, текст запроса поменялся(рис.9 и рис.10).

![Страница авторизации](image/Untitled10.png){#fig:009 width=70%}

![Страница авторизации](image/Untitled13.png){#fig:010 width=70%}

История запросов хранится во вкладке Target (рис.11).

![История запросов](image/Untitled11.png){#fig:010 width=70%}

Я попробую ввести неправильные, случайные данные в веб-приложении и нажмем `Login`. В запросе увидим строку, в которой отображаются введенные нами данные, то есть поле для ввода(рис.12 и рис.13).

![Ввод случайных данных](image/Untitled14.png){#fig:012 width=70%}

![Ввод случайных данных](image/Untitled15.png){#fig:013 width=70%}

Этот запрос так же можно найти во вкладке Target, там же жмем правой кнопкой мыши на хост нужного запроса, и далее нажимаем "Send to Intruder"(рис.14).

![POST-запрос с вводом пароля и логина](image/Untitled17.png){#fig:014 width=70%}

Я попадаю на вкладку Intruder, вижу значения по умолчанию у типа атаки и наш запрос(рис.15).

![Вкладка Intruder](image/Untitled18.png){#fig:015 width=70%}

Я изменяю значение типа атаки на Cluster bomb и проставляю специальные символы у тех данных в форме для ввода, которые буду пробивать(рис.16).

![Изменение типа атаки](image/Untitled20.png){#fig:016 width=70%}

Так как мне нужно параметра для подбора, то нужно списка со значениями для подбора(рис.17).

![Первый Simple list](image/Untitled21.png){#fig:017 width=70%}

Я запускаю атаку и начинаю подбор(рис.18).

![Запуск атаки](image/Untitled23.png){#fig:018 width=70%}

При открытии результата каждого post-запроса можно увидеть полученный get-запрос, в нем видно, куда нас перенаправило после выполнения ввода пары пользователь-пароль. В представленном случае с подбором пары passwd-password нас перенаправило на login.php, это значит, что пара не подходит(рис.19).

![Результат запроса](image/Untitled26.png){#fig:019 width=70%}

Я проверяю результат пары admin-password во вкладке Response, теперь нас перенаправляет на страницу index.php, значит пара должна быть верной(рис.20).

![Результат запроса](image/Untitled27.png){#fig:020 width=70%}

Дополнительная проверка с использованием Repeater, нажимаю на нужный мне запрос правой кнопкой мыши и жмем "Send to Repeater" (рис.21).

![Дополнительная проверка результата](image/Untitled28.png){#fig:021 width=70%}

Я перехожу во вкладку "Repeater"(рис.22).

![Вкладка Repeater](image/Untitled29.png){#fig:022 width=70%}

Нажимаю"send", получаю в Response в результат перенаправление на index.php(рис.23).

![Окно Response](image/Untitled30.png){#fig:023 width=70%}

После нажатия на `Follow redirection`, получим нескомпилированный html код в окне Response(рис.24).

![Изменение в окне Response](image/Untitled31.png){#fig:024 width=70%}

Далее в подокне Render получаю то, как выглядит полученная страница (рис.25).

![Полученная страница](image/Untitled32.png){#fig:025 width=70%}

# Выводы

При выполнении лабораторной работы научилась использовать инструмент Burp Suite.

# Список литературы{.unnumbered}

Ш. Парасрам Т.Х.и.др. А. Замм. Kali Linux: Тестирование на проникновение и безопасность: для профессионалов. Питер, 2022. 448 с.
