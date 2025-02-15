---
## Front matter
title: "Лабораторная работа №1."
subtitle: "Простые модели компьютерной сети"
author: "Александр Андреевич Шуплецов"

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

 Приобретение навыков моделирования сетей передачи данных с помощью средcтва имитационного моделирования NS-2, а также анализ полученных результатов моделирования.

# Выполнение работы

1. Создадим директорию для работы, файл для шаблона.

![создание директории и файла для шаблона](image/1.png){#fig:001 width=70%}

2. Напишем содержимое шаблона.

![содержимое шаблона](image/2.png){#fig:001 width=70%}

3. Напишем простой пример описания топологии сети, состоящей из двух узлов и одного соединения.

![текст простого примера описания топологии сети](image/3.png){#fig:001 width=70%}

4. Вывод простого примера описания топологии сети, состоящей из двух узлов и одного соединения.

![вывод простого примера описания топологии сети](image/4.png){#fig:001 width=70%}

5. Напишем пример с усложненной топологией сети.

![текст примера с усложненной топологией сети](image/5.png){#fig:001 width=70%}

6. Вывод примера с усложненной топологией сети.

![вывод примера с усложненной топологией сети](image/6.png){#fig:001 width=70%}

7. Напишем пример с кольцевой топологией сети.

![текст примера с кольцевой топологией сети](image/7.png){#fig:001 width=70%}

8. Вывод примера с кольцевой топологией сети.

![вывод примера с кольцевой топологией сети](image/8.png){#fig:001 width=70%}

9. Дополним пример с кольцевой топологией сети.

![текст дополненного примера с кольцевой топологией сети](image/9.png){#fig:001 width=70%}

10. Вывод дополненного примера с кольцевой топологией сети.

![вывод дополненного примера с кольцевой топологией сети](image/10.png){#fig:001 width=70%}

# Выводы

Я приобрел навыки моделирования сетей передачи данных с помощью средcтва имитационного моделирования NS-2, а также сделал анализ полученных результатов моделирования.

# Список литературы{.unnumbered}

Королькова А. В., Кулябов Д.С. "Материалы к лабораторным работам"
