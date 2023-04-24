*** Homework_№1 ***
---
+ Посмотреть где я - `pwd`
+ Создать папку - `mkdir foldername`
+ Зайти в папку - `cd foldername`
+ Создать 3 папки - `mkdir name_folder_1 name_folder_2 name_folder_3`
+ Зайти в любоую папку - `cd name_folder_1`
+ Создать 5 файлов (3 txt, 2 json) - `touch file1.txt file2.txt file3.txt doc1.json doc2.json`
+ Создать 3 папки - `mkdir dir_1 dir_2 dir_3`
+ Вывести список содержимого папки `ls -la`
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
