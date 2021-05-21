---
# Front matter
lang: ru-RU
title: "Отчет к лабораторной работе №3"
subtitle: "Дисциплина: операционные системы"
author: "Крупенникова Виктория Александровна"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить идеологию и применение средств контроля версий

# Задание

Сделайте отчёт по предыдущей лабораторной работе в формате Markdown.–В качестве отчёта просьба предоставить отчёты в 3 форматах:pdf,docxиmd(вархиве,поскольку он должен содержать скриншоты,Makefile ит.д.

# Выполнение лабораторной работы

1) Создаю учетную запись на https://github.com.

![Учетная запись](image/1.png){ #fig:001 width=70% }

2) Настраиваю систему контроля версий git. 

3) Синхранизирую учётную запись github с компьютером:
git config --global user.name "Имя Фамилия"
git config --global user.email "work@mail" 

![Настройка системы контроля версий](image/2.png){ #fig:002 width=70% }

4) Создаю новый ключ на github (команда ssh-keygen -C "vakrupennikova <krupka2002@yandex.ru>") и привязываю его к копьютеру через консоль. 

![Создаю новый ключ](image/3.png){ #fig:003 width=70% }

![](image/4.png){ #fig:004 width=70% }

![](image/5.png){ #fig:005 width=70% }

![](image/6.png){ #fig:006 width=70% }

5) В githup захожу в «repositories» и создаю новый репозиторий. Копируем в консоль ссылку на репозиторий.

![Создаю репозиторий](image/7.png){ #fig:007 width=70% }

![](image/8.png){ #fig:008 width=70% }

6) Работаю с каталогом и папками через консоль. Перед тем, как создавать файлы, захожу в репозиорий и создаю файлы: 

![Работа с каталогами и папками](image/9.png){ #fig:009 width=70% }

![](image/10.png){ #fig:010 width=70% }

7) Добавляю первый коммит и выкладываю на githup. Для того, чтобы правильно разместить первый коммит, необходимо добавить команду git add . , далее с помощью команды git commit -m "first commit" выкладываем коммит:

![Выкладываю первый коммит](image/11.png){ #fig:011 width=70% }

8) Сохраняю первый коммит (git push):

![Сохраняю первый коммит](image/12.png){ #fig:012 width=70% }

9) Добавляю файл лицензии (скринкаст оборвался, скриншоты тоже).

10) Добавляю шаблон игнорируемых файлов. Получаю список имеющихся шаблонов.

11) Скачиваю шаблон, например, для C. Также добавляю новые файлы и выполняю коммит.

12)Отправляю на github (git push): 

![Отправляю файлы на github](image/13.png){ #fig:013 width=70% }

13) Инициализирую git-flow, используя команду git flow init -f (префикс для ярлыков установлен в v). Проверяю, что нахожусь на ветке develop (git branch). Создаю релиз с версией 1.0.0. Записываю версию и добавляю в индекс.

echo"1.0.0" >> VERSION

git add .

git commit -am 'chore(main): add version'

14) Заливаю релизную ветку в основную ветку (команда git flow release finish1.0.0).

15) Отправляю данные на github:
git push - -all
git push - -tags 

![Отправляю данные](image/14.png){ #fig:014 width=70% }

16) Создаю релиз на github. Заходим в «Releases», нажимаю «Создать новый релиз». Захожу в теги и заполняю все поля (теги для версии 1.0.0). После создания тега, автоматически сформируется релиз. 

![Релиз](image/15.png){ #fig:015 width=70% }

# Выводы

В ходе выполнения лабораторной работы я изучила идеологию и применение средств контроля версий
