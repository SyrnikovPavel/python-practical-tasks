# Python для решения практических задач

Решение задач курса "Python для решения практических задач" (https://stepik.org/course/4519/)

<h1> Обработка web-страниц </h1>

<h2> 1.1 Скачивание web-страниц </h2>
Мы сохранили страницу с википедии про языки программирования и сохранили по адресу <a href="https://stepik.org/media/attachments/lesson/209717/1.html">https://stepik.org/media/attachments/lesson/209717/1.html</a>
Скачайте её с помощью скрипта на Питоне и посчитайте, какой язык упоминается чаще Python или C++ (ответ должен быть одной из этих двух строк).
<b> Ответ: C++ </b>

<h2> 1.2 Скачивание web-страниц </h2>
Файл <a href="https://stepik.org/media/attachments/lesson/209719/2.html">https://stepik.org/media/attachments/lesson/209719/2.html</a> содержит статью с Википедии про язык Python. В этой статье есть теги code, которыми выделяются конструкции на языке Python. Вам нужно найти все строки, содержащиеся между тегами 'code' и '/code' и найти те строки, которые встречаются чаще всего и вывести их в алфавитном порядке, разделяя пробелами.
Например, если исходный текст страницы выглядел бы так:
<br/><code>< code >a< / code > </code>
<br/><code>< a >bracadabr< /a > </code>
<br/><code>< code >c< / code > </code>
<br/><code>< code >b< / code > </code>
<br/><code>< code >b< / code > </code>
<br/><code>< code >c< / code > </code>
<br/>

то в ответ надо было бы ввести строку "b c".
<br/><b> Ответ: else except finally </b>

<h2> 1.3 Знакомство с BeautifulSoup </h2>
Сейчас вам нужно установить библиотеку BeautifulSoup. Чтобы проверить, что всё установилось хорошо, необходимо запусить код, представленный ниже и сдать в качестве ответа то, что он выводит.
<br/><b> Ответ: 94596065609609271052308 </b>

<h2> 1.4 Использование BeautifulSoup </h2>
В файле <a href="https://stepik.org/media/attachments/lesson/209723/3.html">https://stepik.org/media/attachments/lesson/209723/3.html</a> находится одна таблица. Просуммируйте все числа в ней и введите в качестве ответа одно число - эту сумму. Для доступа к ячейкам используйте возможности BeautifulSoup.
<br/><b> Ответ: 1005425 </b>

<br/>В файле <a href="https://stepik.org/media/attachments/lesson/209723/4.html">https://stepik.org/media/attachments/lesson/209723/4.html</a> находится одна таблица. Просуммируйте все числа в ней. Теперь мы добавили разных тегов для изменения стиля отображения. Для доступа к ячейкам используйте возможности BeautifulSoup.
<br/><b> Ответ: 29536 </b>

В файле <a href="https://stepik.org/media/attachments/lesson/209723/5.html">https://stepik.org/media/attachments/lesson/209723/5.html</a> находится одна таблица. Просуммируйте все числа в ней. Теперь мы не только добавили разных тегов для изменения стиля отображения, но и сделали невалидный HTML-код (правда, браузеры его отображают, а вот с BeautifulSoup могут быть проблемы). Невалидный HTML-код - не редкость в интернете, надо учиться работать и с этим. Вы можете исправить html-код или попробовать использовать нестандартный парсер html, такой как html5lib.
<br/><b> Ответ: 28734 </b>

<h1> Электронные таблицы </h1>
    
<h2> 2.1 Знакомство с электронными таблицами </h2>
Для решения этой задачи необходимо установить библиотеку xlrd, скачать файл <a href="https://stepik.org/media/attachments/lesson/245266/tab.xlsx">https://stepik.org/media/attachments/lesson/245266/tab.xlsx</a> и создать в папке с этим файлом скрипт со следующем содержанием:
<code>
    import xlrd

    wb = xlrd.open_workbook('tab.xlsx')
    sheet_names = wb.sheet_names()
    sh = wb.sheet_by_name(sheet_names[0])
    nmin = sh.row_values(6)[2]
    for rownum in range(7, 27):
        temp = sh.row_values(rownum)
        nmin = min(nmin, temp[2])
    print(nmin)
</code>
<br/><b> Ответ: 39650.2 </b>
    
<h2> 2.2 Работа с одним листом </h2>
Вася планирует карьеру и переезд. Для это составил таблицу, в которой для каждого региона записал зарплаты для разных интересные ему профессий. Таблица доступна по ссылке <a href="https://stepik.org/media/attachments/lesson/245267/salaries.xlsx">https://stepik.org/media/attachments/lesson/245267/salaries.xlsx</a>. Выведите название региона с самой высокой медианной зарплатой (медианой называется элемент, стоящий в середине массива после его упорядочивания) и, через пробел, название профессии с самой высокой средней зарплатой по всем регионам. 
<br/><b> Куала-Лумпур Собачий парикмахер </b>   
