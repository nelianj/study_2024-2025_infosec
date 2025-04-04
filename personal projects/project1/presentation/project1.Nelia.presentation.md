---
## Front matter
lang: ru-RU
title: Презентация по индивидуальнной проекте
subtitle: Основы информационной безопасности
author:
  - Нджову Н.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 27 февралья 2025

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

Приобретение практических навыков по установке операционной системы Linux на витуальную машину.

## Задание

1. Установить Kali Linux на витуальную машину.

## Выполнение лабораторной работы

Я создала новую виртуальную машину, указивая имя и образ ISO(рис.1)

![создание виртуальной машины](image/Untitled1.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я указывала размер основной памяти виртуальной машины и выбрала количество процессора(рис.2)

![указание размера основной памяти виртуальной машины](image/Untitled2.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я установила размер диска на 40ГБ(рис.3)

![Окно определения размера виртуального динамического жёсткого диска и его расположения](image/Untitled3.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я согласилася с полученными характеристиками(рис.4)

![создание виртуальной машины](image/Untitled4.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я проверяла подключен ли образ диска к носителю(рис.5)

![создание виртуальной машины](image/Untitled5.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я запускала виртуальную машину(рис.6)

![запуск виртуальную машину](image/Untitled6.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбрала English в качестве языка интерфейс(рис.7)

![выбор языка](image/Untitled7.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбрала место(рис.8)

![выбор места](image/Untitled8.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбрала языки раскладки клавиатуры(рис.9)

![языки раскладки клавиатуры](image/Untitled9.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я ввела имя компьютера(рис.10)

![Ввод имени компьютера](image/Untitled10.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я ввела имя домена(рис.11)

![Ввод имени домена](image/Untitled11.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я ввела имя пользователя(рис.12)

![Ввод имени пользователя](image/Untitled12.png){#fig:001 width=70%}

## Выполнение лабораторной работы

По умолчанию, это же имя предлагается как имя моей учетной записи-с маленькими буквами(рис.13)

![Ввод имени моей учетной записи](image/Untitled16.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я ввела пароль для созданного пользователя(рис.14)

![создание пароля](image/Untitled17.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я выбирала часовой пояс(рис.15)

![часовой пояс](image/Untitled32.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Установщик проверяла диски и предлагала различные варианты, в зависимости от настроек. Созданный виртуальный диск чистый, поэтому я выбирала весь диск(entire disk)(рис.16)

![Разметка дисков](image/Untitled19.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Затем я выбирала нужный виртуальный диск(рис.17)

![Разметка дисков](image/Untitled20.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Далее установщик предлагала выбрать схему разметки, ее я оставляла по умолчанию все файлы в одном разделе(all files in one partition)(рис.18)

![Разметка дисков](image/Untitled21.png){#fig:001 width=70%}

## Выполнение лабораторной работы

После этого я подтвердила окончание разбиения диска, чтобы изменения были записаны(рис.19)

![окончание разметка дисков](image/Untitled22.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Затем установщик позволяет вам еще раз просмотреть конфигурацию диска, прежде чем вносить постоянные изменения. После этого этапа начнется установка(рис.20)

![окончание разметка дисков](image/Untitled23.png){#fig:001 width=70%}

## Выполнение лабораторной работы

После этого этапа начнется установка(рис.21)

![установка](image/Untitled24.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Дальше я выбрала какой метапакеты (пустые пакеты, описывающие только зависимости), которые я хотела установить(рис.22)

![Выбор программного обеспечения](image/Untitled25.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я подтвердила установку системы загрузчика системы GRUB из проекта GNU (программа для управления процессом загрузки),я также выбирала виртуальный диск, на который будет установлен GRUB(рис.23)

![становка системного загрузчика](image/Untitled28.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я завершала установку(рис.24)

![Завершение установки](image/Untitled29.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я проверяла, что в носителях теперь пусто(рис.25)

![Проверка носителей](image/Untitled30.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Я входила в систему от имени своего пользователя(рис.26)

![вход в систему](image/Untitled31.png){#fig:001 width=70%}

## Выполнение лабораторной работы

Это выполнен успешно(рис.27)

![Успешная загрузка системы](image/Untitled34.png){#fig:001 width=70%}

# Выводы

Выполнив эту работу, я приобрела практические навыки по установке операционной системы Linux на витуальную машину.

