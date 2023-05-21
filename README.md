# HOMEWORK_№1

***1. Посмотреть где я:***
> `pwd`
-----------------------------
***2. Создать папку:***
> `mkdir foldername`
-----------------------------
***3. Зайти в папку:***
> `cd foldername`
-----------------------------
***4. Создать 3 папки:***
> `mkdir name_folder_1 name_folder_2 name_folder_3`
-----------------------------
***5. Зайти в любоую папку:***
> `cd name_folder_1`
-----------------------------
***6. Создать 5 файлов (3 txt, 2 json):***
> `touch file1.txt file2.txt file3.txt doc1.json doc2.json`
-----------------------------
***7. Создать 3 папки:***
> `mkdir dir_1 dir_2 dir_3`
-----------------------------
***8. Вывести список содержимого папки:***
> `ls -la`
-----------------------------
+ Открыть любой txt файл + написать туда что-нибудь, любой текст + сохранить и выйти - `vim file1.txt -i ....` `ESC :wq`
+ Выйти из папки на уровень выше - `cd ..`
+ Переместить любые 2 файла, которые вы создали, в любую другую папку - `mv ./name_folder_1/{file1.txt,file2.txt} D:/foldername/name_folder_2/`
+ Cкопировать любые 2 файла, которые вы создали, в любую другую папку `cp ./name_folder_1/{doc1.json,doc2.json} D:/foldername/name_folder_3/`
+ Найти файла по имени - `find . -name file3.txt`
+ Просмотреть содержимое в реальном времени (команда grep) изучите как она работает - `tail -f file2.txt`
+ Вывести несколько первых строк из текстового файла - `head -n 4 file1.txt`
+ Вывести несколько последних строк из текстового файла - `tail -n 4 file3.txt`
+ Посмотреть содержимое длинного файла команда `less file3.txt`
+ Вывести дату и время - `date`
+ Отправить http-запрос на сервер http://162.55.220.72:5005/terminal-hw-request - `curl http://162.55.220.72:5005/terminal-hw-request`
+ Получаем заголовки от сервера - `curl -i http://162.55.220.72:5005/terminal-hw-request`
+ Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

    * `nano firstscript.sh` - открываем редактор и задаём имя скрипта
    * `#!/bin/bash` - указатель что это оболочка bash
    * `cd foldername`
    * `mkdir folder_1 folder_2 folder_3`
    * `cd folder_1`
    * `touch f_1.txt f_2.txt f_3.txt d_1.json d_2.json`
    * `mkdir catalog_1 catalog_2 catalog_3`
    * `ls -la`
    * `mv ./folder_1/{f_1.txt,f_2.txt} D:/foldername/folder_2/`
    * `CTRL + D` - выходим и сохраняем скрипт   
    * `chmod +x ./firstscript` - делаем скрипт исполняемым
    * `./firstscript` - запускаем скрипт
---

# HOMEWORK_№2
+ Сделать папку dir_1 - `mkdir dir_1`
+ Зайти в папку dir_1 - `cd dir_1`
+ Создать папку inner_dir_1 - `mkdir inner_dir_1`
+ Посмотреть где ты находишься - `pwd`
+ Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt - `touch tf_1.txt`
+ Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками: - the first 1 - the second 2 - the third 3
`cat > tf_2.txt - the first 1 - the second 2 - the third 3`
+ Зайти в папку inner_dir_1 - `cd inner_dir_1`
+ Через cat сделать текстовый файл tf_3.txt  c любыми строками - `cat > tf_3.txt ......`
+ Через cat добавить в текстовый файл tf_3.txt строку 'the second 2' - `cat >> tf_3.txt` 'the second 2'
+ Через cat добавить в текстовый файл tf_3.txt строку 'the sec 2' - `cat >> tf_3.txt` 'the sec 2'
+ Через cat добавить в текстовый файл tf_2.txt строку 'the sec 3' - `cat >> D:/dir_1/tf_2.txt 'the sec 3'`        
+ Через cat добавить в текстовый файл tf_3.txt строку 'the SeCoNd 2' - `cat >> tf_3.txt` 'the SeCoNd 2'
+ Через cat добавить в текстовый файл tf_2.txt строку 'the seConD 2' - `cat >> tf_2.txt` 'the seConD 2'
+ Сделать текстовый файл tf_4.txt в котором будет 15 строк - `cat > tf_4.txt .....` 
+ Сделать текстовый файл tF_5.txt в котором будет 13 строк - `cat > tF_5.txt .....` 
+ Вывести список всех файлов в папке - `find`
+ Выйти из папки inner_dir_1 - `cd ..`
+ Вывести содержимое файла tf_3.txt в терминал - `cat D:/dir_1/inner_dir_1/tf_3.txt`
+ Найти путь к файлу tf_4.txt - `realpath tf_4.txt`
+ Отчистить файл tf_4.txt от содержимого без удаления самого файла - `> D:/dir_1/inner_dir_1/tf_4.txt`
+ Найти путь к файлам у которых есть  'tf' в названии - `find . -name '*tf*'`
+ Найти путь к файлам у которых есть  'tf' в названии и буквы в любом регистре - `find . -iname '*tf*'`
+ Найти строки в файлах где есть комбинация букв 'sec' в текущей папке - `grep -r 'sec'` 
+ Найти строки в файлах где есть комбинация букв 'sec' в любом регистре в текущей папке - `grep -r -i 'sec'`                                                        
+ Найти строки в файлах где есть только комбинация букв 'sec' в текущей папке - `grep -r -w 'sec'`
+ Найти строки в файлах где есть только комбинация букв 'sec' в любом регистре в текущей папке - `grep -r -i -w 'sec'`
+ Найти строки в файлах где есть комбинация букв 'second' в текущей папке - `grep -r 'second'`
+ Найти строки в файлах где есть комбинация букв 'second' в любом регистре в текущей папке - `grep -r -i 'second'`
+ Найти строки в файлах где есть комбинация букв 'second' во всех папках ниже уровнем - `grep 'second' ./*`
+ Найти только путь и название файла в строках которых есть комбинация букв 'second' в текущей папке - `grep -r -l 'second'`
+ Найти все строки во всех файлах где нет комбинации 'second' - `grep -r -v 'second'`
+ Найти только название и путь к файлам где нет комбинации 'second' - `grep -rlv 'second'`
+ Вывести в терминал 4 последних строк любого текстового файла - `tail -n 4 ./inner_dir-1/tf_3.txt`
+ Вывести в терминал 4 первые строки любого текстового файла - `head -n 4 ./inner_dir-1/tf_3.txt`
+ Команда в одну строку. Создать папку и создать текстовый файл с содержиммым - `mrkdir folder | echo This is my bash practice > tf_6.txt (файл tf_6.txt будет создан вне новой папки)`.
+ Команда в одну строку созадать папку внутри с файлом содержащий текст - `mkdir NEW_FOLDER && cd NEW_FOLDER && echo "Text" >> TF_10.txt`
+ Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово 'sec' - `grep -rl 'sec' * | xargs mv -t D:/dir_1/folder`
+ Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово 'sec' - `grep -rl 'sec' * | xargs cp -t D:/dir_1/folder`
+ Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл - `grep -r 'sec' * >> newfile.txt`
+ Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово 'sec' - `grep -rl 'sec' * | xargs rm -rf`
+ Просто вывести в терминал строку “Good job!!” - `echo 'Good job!!'`
