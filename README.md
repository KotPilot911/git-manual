Список комманд для работы с Git
================================
Навигация  
---
<br>
pwd (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке;
<br>
ls (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;
<br>
ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;
<br>
cd first-project (от англ. change directory, «сменить директорию») — перейди в папку first-project;
<br>
cd first-project/html — перейди в папку html, которая находится в папке first-project;
<br>
cd .. — перейди на уровень выше, в родительскую папку;
<br>
cd ~ — перейди в домашнюю директорию (/Users/Username);
<br>
cd / — перейди в корневую директорию.
<br>
<br>

Работа с файлами и папками  
---

<br>

Создание  
---  

<br>
touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке;
<br>
touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;
<br>
mkdir second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке.
<br>

Копирование и перемещение  
---
   
<br>
cp file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место;
<br>
mv file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место.
<br>

Чтение  
---
  
<br>
cat file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt.
<br>

Удаление   
---  

<br>
rm about.html (от англ. remove, «удалить») — удали файл about.html;
<br>
rmdir images (от англ. remove directory, «удалить директорию») — удали папку images;
<br>
rm -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.
<br>

Полезные возможности  
--- 
   
<br>
Команды необязательно печатать и выполнять по очереди. Можно указать их списком — разделить двумя амперсандами (&&).
<br>
У консоли есть собственная память — буфер с несколькими последними командами. По ним можно перемещаться с помощью клавиш со стрелками вверх (↑) и вниз (↓).
<br>
Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать Tab. 
<br>
Если файл или папка есть в текущей директории, командная строка допишет путь сама.
<br>
Например, вы находитесь в папке dev. Начните вводить cd first и дважды нажмите Tab. 
<br>
Если папка first-project есть внутри dev, командная строка автоматически подставит её имя. 
<br>
Останется только нажать Enter.
<br>

Работа с Git и коммитами
============================================================

Сделать папку репозиторием — git init
---

Чтобы Git начал отслеживать изменения в проекте, папку с файлами этого проекта нужно сделать Git-репозиторием (от англ. repository — «хранилище»). Для этого следует переместиться в неё и ввести команду git init (от англ. initialize — «инициализировать»).
Например, создайте папку first-project и сделайте её Git-репозиторием: перейдите в неё с помощью команды cd и выполните git init.

```
$ cd ~/dev/first-project # перешли в нужную папку

$ git init # создали репозиторий 
```

Вы можете создать папку в любом месте на компьютере. Но в этом случае не забывайте менять в наших примерах путь ~/dev/first-project на тот, который ведёт к вашей папке. Помните, что не рекомендуется создавать репозиторий Git внутри другого Git-репозитория. Это может вызывать проблемы с отслеживанием изменений.

В некоторых случаях при инициализации репозитория Git может показать объёмное сообщение, которое начинается со слов Using 'master' as the name…. Не пугайтесь: это не ошибка. Пока это сообщение не имеет большого значения.

Также git init выведет сообщение вида Initialized empty Git repository in <*ваша папка с проектом*>/.git/ (англ. «инициализирован пустой Git-репозиторий в <*ваша папка*>/.git/»). В подпапке .git Git будет хранить всю служебную информацию.

Команда git init — одна из редко применяемых, ведь репозиторий создаётся один раз, а пользоваться им можно сколько угодно долго.
<br>
Если вы случайно сделали Git-репозиторием не ту папку, её можно «разгитить». 

Для этого нужно удалить скрытую подпапку .git.
```
$ cd <папка с репозиторием> # перешли в папку

$ rm -rf .git # удалили подпапку .git 
```

