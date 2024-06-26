---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №6
subtitle: "Мандатное разграничение прав в Linux"
author:
  - Галацан Николай
institute:
  - Российский университет дружбы народов, Москва, Россия

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


## Докладчик

  * Галацан Николай
  * 1032225763
  * уч. группа: НПИбд-01-22
  * Факультет физико-математических и естественных наук
  * Российский университет дружбы народов

## Цели и задачи

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux.
Проверить работу SELinx на практике совместно с веб-сервером Apache.

## Выполнение лабораторной работы

![Режим работы SELinux, статус httpd](image/1.png){#fig:1 width=50%}

## Выполнение лабораторной работы

![Контекст безопасности веб-сервера Apache, состояние переключателей SELinux](image/2.png){#fig:2 width=60%}

## Выполнение лабораторной работы

![Статистика по политике](image/3.png){#fig:3 width=70%}

## Выполнение лабораторной работы

![Просмтр файлов, создание test.html и просмотр контекста](image/4.png){#fig:4 width=70%}

## Выполнение лабораторной работы

![Запуск файла в браузере](image/5.png){#fig:5 width=70%}

## Выполнение лабораторной работы

![Изменение контекста файла и попытка просмотра](image/6.png){#fig:6 width=70%}

## Выполнение лабораторной работы

![Просмотр лог-файла](image/7.png){#fig:7 width=50%}

## Выполнение лабораторной работы

![Изменение порта в конфигурационном файле](image/8.png){#fig:8 width=70%}

## Выполнение лабораторной работы

![Сбой веб-сервера](image/9.png){#fig:9 width=70%}

## Выполнение лабораторной работы

![Просмотр лог-файла](image/10.png){#fig:10 width=70%}

## Выполнение лабораторной работы

![Добавление порта 81 и проверка. Перезапуск веб-сервера. Возвращение контекста](image/11.png){#fig:11 width=50%}

## Выполнение лабораторной работы

![Завершение выполнения работы](image/12.png){#fig:12 width=70%}

## Выводы

Я развил навыки администрирования ОС Linux, познакомился с технологией SELinux. Проверена работа SELinux на практике совместно с веб-сервером Apache.

