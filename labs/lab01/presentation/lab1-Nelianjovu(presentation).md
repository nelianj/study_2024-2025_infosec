---
## Front matter
lang: ru-RU
title: Структура научной презентации
subtitle: Простейший шаблон
author:
  - Нджову Н.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 18 февраля 2025
Структура научной презентации
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

## Задание

1. Установка и настройка операционной системы.

2. Найти следующую информацию:
    1. Версия ядра Linux (Linux version).

    2. Частота процессора (Detected Mhz processor).

    3. Модель процессора (CPU0).

    4. Объем доступной оперативной памяти (Memory available).

    5. Тип обнаруженного гипервизора (Hypervisor detected).

    6. Тип файловой системы корневого раздела

## Выполнение лабораторной работы

Я создала новую виртуальную машину, указивая имя и образ ISO(рис.1).

![создание виртуальной машины](image/Untitled1.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбрала имя пользователя и имя хоста(рис.2)

![установки гостевой оси](image/Untitled30.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я указывала размер основной памяти виртуальной машины и выбрала количество процессора(рис.3)

![указание размера основной памяти виртуальной машины](image/Untitled2.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я установила размер диска на 40ГБ(рис.4)

![Окно определения размера виртуального динамического жёсткого диска и его расположения](image/Untitled3.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Проверяю подключен ли образ диска к носителю(рис.5)

![подключение образа оптического диска](image/Untitled5.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я запускала виртуальную машину(рис.6)

![запуск виртуальную машину](image/Untitled6.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбрала English в качестве языка интерфейс(рис.7)

![выбор языка](image/Untitled8.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я скорректировала часовой пояс и место(рис.8)

![часовой пояс](image/Untitled11.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбрала языки раскладки клавиатуры и задала комбинацию клавиш для переключения между раскладками клавиатуры (рис.9)

![языки раскладки клавиатуры](image/Untitled10.png){#fig:001 width=70%}

## Выполнение лабораторной работы

В разделе выбора программы в качестве базовой среды указывала Server with GUI, а в качестве дополнения - Development tools(рис.10)

![настройка установки: выбор программ](image/Untitled12.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я отключила KDUMP (рис.11)

![отключение KDUMP](image/Untitled17.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я включила сетевое подключение и задала имя хоста(рис.12)

![сеть и имя узла](image/Untitled14.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я установила пароль для root и пользователя с правами администратора(рис.13)

![пароль для root](image/Untitled15.png){#fig:001 width=70%}

![пользователя с правами администратора](image/Untitled33.png){#fig:001 width=70%}

## Выполнение лабораторной работы

После завершения установки операционной системы я перезагрузилая и запустила виртуальную машину(рис.14)

![Завершение установки ОС](image/Untitled19.png){#fig:001 width=70%}

## Выполнение лабораторной работы

В VirtualBox оптический привод должен автоматически отключиться(рис.15)

![проверка носителей](image/Untitled34.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я вошла в ОС, используя учетную запись, созданную во время установки(рис.16)

![входа в ос](image/Untitled22.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Я открывала терминал и запускала команда dmesg | less(рис.17)

![команда dmesg | less](image/Untitled24.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Я использовала поиск с помощью grep-dmesg | grep -i "то, что ищем", и получила следующую информацию:

Версия ядра Linux (Linux version)(рис.18)

![Версия ядра Linux](image/Untitled25.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Частота процессора (Detected Mhz processor)(рис.19)

![Частота процессора](image/Untitled38.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Модель процессора (CPU0)(рис.20)

![Модель процессора](image/Untitled27.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Объем доступной оперативной памяти (Memory available)(рис.21)

![оперативной памяти](image/Untitled28.png){#fig:001 width=70%}
Структура научной презентации
## Выполнение дополнительного задания

Тип обнаруженного гипервизора (Hypervisor detected)(рис.22)

![Тип обнаруженного гипервизора](image/Untitled29.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Тип файловой системы корневого раздела(рис.23)

![Тип файловой системы](image/Untitled36.png){#fig:001 width=70%}

## Выполнение дополнительного задания

Последовательность монтирования файловых систем

![Последовательность монтирования файловых систем](image/Untitled37.png){#fig:001 width=70%}

## Выводы

Выполнив эту лабораторной работы, я приобрела практических навыков установки операционной системы на виртуальную машину и настройки минимально необходимых для дальнейшей работы сервисов.
