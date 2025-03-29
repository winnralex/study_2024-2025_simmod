---
## Front matter
title: "Лабораторная работа № 8"
subtitle: "Модель TCP/AQM"
author: "Шуплецов Александр Андреевич"

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
lot: false # List of tables
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

# Введение

## Цели и задачи

Реализовать модель TCP/AQM с помощью xcos и OpenModelica.

# Выполнение лабораторной работы

## Реализация модели в xcos

Зададим переменное окружение(рис. [-@fig:001]).

![Переменное окружение](image/1.png){#fig:001 width=70%}

Затем реализуем модель TCP/AQM и разместим регистрирующие устройства(рис. [-@fig:002]):

![Модель TCP/AQM в xcos](image/2.png){#fig:002 width=70%}

Получим динамику изменения размера TCP окна W(t)(зеленая линия) и размера очереди Q(t)(черная линия), а также фазовый портрет. (рис. [-@fig:003], [-@fig:004]):

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t)](image/3.png){#fig:003 width=70%}

![Фазовый портрет (W, Q)](image/4.png){#fig:004 width=70%}

Уменьшив скорость обработки пакетов C до 0.9 можно увидеть, что автоколебания стали более выраженными(рис. [-@fig:005], [-@fig:006]).

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t) при С = 0.9](image/5.png){#fig:005 width=70%}

![Фазовый портрет (W, Q) при С = 0.9](image/6.png){#fig:006 width=70%}

## Реализация модели в OpenModelica

Перейдем к реализации модели в OpenModelica. Зададим параметры, переменные и систему уравнений(рис. [-@fig:007]):

![Модель TCP/AQM в OpenModelica](image/7.png){#fig:007 width=70%}

Затем установим параметры симуляции(рис. [-@fig:008]).

![Установки симуляции OpenModelica](image/8.png){#fig:008 width=70%}

Получим динамику изменения размера TCP окна W(t)(зеленая линия) и размера очереди Q(t)(черная линия), а также фазовый портрет, который показывает наличие автоколебаний параметров системы — фазовая траектория осциллирует вокруг своей стационарной точки(рис. [-@fig:009], [-@fig:010]):

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t). OpenModelica](image/9.png){#fig:009 width=70%}

![Фазовый портрет (W, Q). OpenModelica](image/10.png){#fig:010 width=70%}

# Выводы

В результате выполнения работы я реализовал модель TCP/AQM с помощью xcos и OpenModelica.
