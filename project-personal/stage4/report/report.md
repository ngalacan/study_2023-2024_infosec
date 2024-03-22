---
## Front matter
title: "Отчет по этапу №4"
subtitle: "Использование nikto"
author: "Галацан Николай, НПИбд-01-22"

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

Научиться использовать инструмент для сканирования на уязвимости nikto.

# Выполнение лабораторной работы

**nikto** — базовый сканер безопасности веб-сервера. Он сканирует и обнаруживает уязвимости в веб-приложениях, обычно вызванные неправильной конфигурацией на самом сервере, файлами, установленными по умолчанию, и небезопасными файлами, а также устаревшими серверными приложениями. 

Для сканирования цели необходимо ввести `nikto -h <цель> -p <порт>`, где `<цель>` — домен или IP-адрес целевого сайта, а `<порт>` — порт, на котором запущен сервис [@kali-linux].

Для получения справки ввожу `nikto -h`  (рис. [-@fig:1]). 

![Справка](image/1.png){#fig:1 width=70%}

Запускаю сканирование для веб-сайта `gazel.me`. В результате выводятся различные замечания и потенциальные уязвимости (например, уязвимость с кодом CVE-2003-1243) (рис. [-@fig:2]).

![Сканирование веб-сайта](image/2.png){#fig:2 width=70%}

Запускаю сканирование для локальной сети, введя `nikto -h 127.0.0.1`. В результате получаю замечаю о работе сервера Apache (рис. [-@fig:3]).

![Сканирование локальной сети](image/3.png){#fig:3 width=70%}

Далее приступаю к сканированию веб-приложения DVWA, запущенном в локальной сети [@nikto-info] (рис. [-@fig:4]):

![Сканирование DVWA](image/4.png){#fig:4 width=70%}

`nikto` выводит информацию о структуре DVWA и находит возможные уязвимости. Среди них, например, PHP backdoor file manager.

# Выводы

Приобретены навыки использования nikto для сканирования веб-серверов на уязвимости. Сканер nikto позволяет идентифицировать уязвимости веб-приложений, такие как раскрытие информации, инъекция (XSS/Script/HTML), удаленный поиск
файлов (на уровне сервера), выполнение команд и идентификация программного обеспечения.

# Список литературы{.unnumbered}

::: {#refs}
:::

