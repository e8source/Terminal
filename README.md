# Terminal

gitbash

1. Посмотреть где я.
       
       pwd 
2. Создать папку.
       
       mkdir partition
3. Зайти в папку.
       
       cd ./partition
4. Создать 3 папки.
       
       mkdir partition_1 partition_2 partition_3
5. Зайти в любую папку.

       cd ./partition_1 
6. Создать 5 файлов (3 txt, 2 json).

       touch file.txt file_1.txt file_2.txt file_3.json file_4.json
7. Создать 3 папки.
   
       mkdir partition_1_1 partition_1_2 partition_1_3
8. Вывести список содержимого папки.

       ls
9. Открыть любой txt файл.

       nano file_4.json
10. Написать в файл любой текст.
11. Cохранить и выйти.
12. Выйти из папки на уровень выше.

        cd ..
13. Переместить любые 2 файла, которые вы создали, в любую другую папку.

        mv file.txt file_1.txt ../partition_2
14. Cкопировать любые 2 файла, которые вы создали, в любую другую папку.

        cp file_3.json file_4.json ../partition_3
15. Найти файл по имени.
        
        find . -name file_2.txt
16. Просмотреть содержимое в реальном времени.

        tail -f file_4.json
17. Вывести несколько первых строк из текстового файла.

        head -4 file_4.json
18. Вывести несколько последних строк из текстового файла.

        tail -4 file_4.json
19. Просмотреть содержимое длинного файла (команда less) изучите как она работает.
    
        less file_4.json
20. Вывести дату и время.

        date
21. Отправить http запрос на сервер http://162.55.220.72:5005/terminal-hw-request

        curl http://162.55.220.72:5005/terminal-hw-request
22. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13.

	    #!/bin/bash
	    cd ./partition
	    mkdir partition_1 partition_2 partition_3
	    cd ./partition_1
	    touch file.txt file_1.txt file_2.txt file_3.json file_4.json
        mkdir partition_1_1 partition_1_2 partition_1_3
        ls
        mv file.txt file_1.txt file_2.txt ../partition_2

23. Сделать папку dir1

        mkdir dir1
24. Зайти в папку dir1
       
        cd ./dir1
25. Создать папку subdir1
       
        mkdir subdir1 
26. Посмотреть где ты находишься.
       
        pwd
27. Находясь в папке dir1 создать пустой текстовый файл ab1.txt
       
        touch ab1.txt
28. Находясь в папке dir1 через команду cat создать текстовый файл ab2.txt со следующими строками:
- is the first 1 
- is the second 2
- is the third 3

      cat > ab2.txt
      is the first 1 
	  is the second 2
	  is the third 3
29. Зайти в папку subdir1
       
        cd subdir1
30. Через cat сделать текстовый файл ab3.txt  c любыми строками.

        cat > ab3.txt
        string 1
        string 2
        string 3
31. Через cat добавить в текстовый файл ab3.txt строку “is the second 2”

       cat >> ab3.txt <<< "is the second 2"
32. Через cat добавить в текстовый файл ab3.txt строку “is the sec 2”

        cat >> ab3.txt <<< "is the sec 2"
33. Через cat добавить в текстовый файл ab2.txt строку “is the sec 3” 
        
        cat >> ../ab2.txt <<< "is the sec 3"
34. Через cat добавить в текстовый файл ab3.txt строку “is the SeCoNd 2”
        
        cat >> ab3.txt <<< "is the SeCoNd 2"
35. Через cat добавить в текстовый файл ab2.txt строку “is the seConD 2” 
        
        cat >> ../ab2.txt <<< "is the seConD 2"
36. Сделать текстовый файл ab4.txt в котором будет 12 строк. 
        
        for i in {1..12}; do echo "is the string" >> ab4.txt; done
37. Сделать текстовый файл aB5.txt в котором будет 10 строк. 
        
        for i in {1..10}; do echo "is the line" >> aB5.txt; done
38. Вывести список всех файлов в папке. 
        
        ls
39. Выйти из папки subdir1 
        
        cd ..
40. Вывести содержимое файла ab3.txt в терминал. 
        
        cat subdir1/ab3.txt
41. Найти путь к файлу ab4.txt 
        
        find . -name ab4.txt -type f
42. Очистить файл ab4.txt от содержимого без удаления самого файла. 
        
        echo "" > subdir1/ab4.txt
43. Найти путь к файлам у которых есть “ab” в названии. 

        find . -name "*ab*" -type f
44. Найти путь к файлам у которых есть “ab” в названии и буквы в любом регистре. 
        
        find . -iname "*ab*" -type f
45. Найти строки в файлах где есть комбинация букв “sec” в текущей папке.
        
        grep "sec" *
46. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке.
        
        grep -i "sec" *
47. Найти строки в файлах где есть слово “sec” в текущей папке.
        
        grep -w "sec" *
48. Найти строки в файлах где есть слово “sec” в любом регистре в текущей папке.
        
        grep -i -w "sec" *
49. Найти строки в файлах где есть комбинация букв “second” в текущей папке.
        
        grep "second" *
50. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке.
        
        grep -i "second" *
51. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем.
        
        grep -r "second" *
52. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке.
        
        grep -l "second" *
53. Найти все строки во всех файлах где нет комбинации “second”
        
        grep -v "second" *
54. Найти только название и путь к файлам где нет комбинации “second” 
        
        grep -lv "second" *
55. Вывести в терминал 2 последних строк любого текстового файла.
        
        tail -2 ab2.txt
56. Вывести в терминал 2 первые строки любого текстового файла. 
        
        head -2 ab2.txt
57. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым.  
        
        mkdir subdir2 && echo "is not the string" > subdir2/ab6.txt
58. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”  
        
        grep -rlw "sec" | xargs -I{} mv {} ./subdir2
59. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”    
        
        grep -rlw "sec" | xargs -I{} cp {} ./subdir1
60. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл. 
        
        grep -r "sec" | xargs echo >> Ab7.txt
61. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “SeCoNd” 
        
        grep -rlw "SeCoNd" | xargs -I{} rm {}
62. Вывести в терминал строку “End of session” 
        
        print End of session
