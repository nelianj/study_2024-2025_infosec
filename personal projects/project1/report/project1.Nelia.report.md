---
## Front matter
title: "Отчёта по индивидуальнной проекте 1"
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

Приобретение практических навыков по установке операционной системы Linux на витуальную машину.

# Задание

1. Установить Kali Linux на витуальную машину.

# Выполнение лабораторной работы

Я создала новую виртуальную машину, указивая имя и образ ISO(рис.1)

![создание виртуальной машины](image/Untitled1.png){#fig:001 width=70%}

Я указывала размер основной памяти виртуальной машины и выбрала количество процессора(рис.2)

![указание размера основной памяти виртуальной машины](image/Untitled2.png){#fig:001 width=70%}

Я установила размер диска на 40ГБ(рис.3)

![Окно определения размера виртуального динамического жёсткого диска и его расположения](image/Untitled3.png){#fig:001 width=70%}

Я согласилася с полученными характеристиками(рис.4)

![создание виртуальной машины](image/Untitled4.png){#fig:001 width=70%}

Я проверяла подключен ли образ диска к носителю(рис.5)

![создание виртуальной машины](image/Untitled5.png){#fig:001 width=70%}

Я запускала виртуальную машину(рис.6)

![запуск виртуальную машину](image/Untitled6.png){#fig:001 width=70%}

Я выбрала English в качестве языка интерфейс(рис.7)

![выбор языка](image/Untitled7.png){#fig:001 width=70%}

Я выбрала место(рис.8)

![выбор места](image/Untitled8.png){#fig:001 width=70%}

Я выбрала языки раскладки клавиатуры(рис.9)

![языки раскладки клавиатуры](image/Untitled9.png){#fig:001 width=70%}

Я ввела имя компьютера(рис.10)

![Ввод имени компьютера](image/Untitled10.png){#fig:001 width=70%}

Я ввела имя домена(рис.11)

![Ввод имени домена](image/Untitled11.png){#fig:001 width=70%}

Я ввела имя пользователя(рис.12)

![Ввод имени пользователя](image/Untitled12.png){#fig:001 width=70%}

По умолчанию, это же имя предлагается как имя моей учетной записи-с маленькими буквами(рис.13)

![Ввод имени моей учетной записи](image/Untitled16.png){#fig:001 width=70%}

Я ввела пароль для созданного пользователя(рис.14)

![создание пароля](image/Untitled17.png){#fig:001 width=70%}

Я выбирала часовой пояс(рис.15)

![часовой пояс](image/Untitled32.png){#fig:001 width=70%}

Установщик проверяла диски и предлагала различные варианты, в зависимости от настроек. Созданный виртуальный диск чистый, поэтому я выбирала весь диск(entire disk)(рис.16)

![Разметка дисков](image/Untitled19.png){#fig:001 width=70%}

Затем я выбирала нужный виртуальный диск(рис.17)

![Разметка дисков](image/Untitled20.png){#fig:001 width=70%}

Далее установщик предлагала выбрать схему разметки, ее я оставляла по умолчанию все файлы в одном разделе(all files in one partition)(рис.18)

![Разметка дисков](image/Untitled21.png){#fig:001 width=70%}

После этого я подтвердила окончание разбиения диска, чтобы изменения были записаны(рис.19)

![окончание разметка дисков](image/Untitled22.png){#fig:001 width=70%}

Затем установщик позволяет вам еще раз просмотреть конфигурацию диска, прежде чем вносить постоянные изменения. После этого этапа начнется установка(рис.20)

![окончание разметка дисков](image/Untitled23.png){#fig:001 width=70%}

После этого этапа начнется установка(рис.21)

![установка](image/Untitled24.png){#fig:001 width=70%}

Дальше я выбрала какой метапакеты (пустые пакеты, описывающие только зависимости), которые я хотела установить(рис.22)

![Выбор программного обеспечения](image/Untitled25.png){#fig:001 width=70%}

Я подтвердила установку системы загрузчика системы GRUB из проекта GNU (программа для управления процессом загрузки),я также выбирала виртуальный диск, на который будет установлен GRUB(рис.23)

![становка системного загрузчика](image/Untitled28.png){#fig:001 width=70%}

Я завершала установку(рис.24)

![Завершение установки](image/Untitled29.png){#fig:001 width=70%}

Я проверяла, что в носителях теперь пусто(рис.25)

![Проверка носителей](image/Untitled30.png){#fig:001 width=70%}

Я входила в систему от имени своего пользователя(рис.26)

![вход в систему](image/Untitled31.png){#fig:001 width=70%}

Это выполнен успешно(рис.27)

![Успешная загрузка системы](image/Untitled34.png){#fig:001 width=70%}

# Выводы

Выполнив эту работу, я приобрела практические навыки по установке операционной системы Linux на витуальную машину.

