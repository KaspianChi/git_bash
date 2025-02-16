# Работа с командами в git_bash

### Задание 1.
[Ссылка на документ](https://github.com/KaspianChi/git_bash/blob/main/bash1.txt)

### 1. Откройте домашнюю директорию через терминал :
cd ~

### 2.Определите имя папки, в которой вы находитесь :
pwd

### 3. Создайте каталог test1 внутри текущей папки :
mkdir test1

### 4.Перейдите в папку test1 :
cd test1

### 5. Создайте файлы 1, 2 и 3 внутри каталога test1 :
touch 1 2 3

### 6. Проверьте содержимое каталога test1 :
ls

### 7. Перейдите в домашнюю директорию :
cd ~

### 8. Создайте папку test2 внутри домашней директории :
mkdir test2

### 9. Удалите папку test2 :
rmdir test2

### 10. Удалите файл 2 из папки test1 :
cd test1

rm 2

### 11. Создайте папку test3 в домашней директории и добавьте в нее два файла :
cd ..

mkdir test3

cd test3

touch file1 file2

### 12. Удалите папку test3 :
cd ..

rm -r test3

### 13. Создайте папку test4 в домашней директории :
mkdir test4

### 14. Переместите файлы 1 и 3 из папки test1 в папку test4 :
mv test1/1 test1/3 TEST4/

### 15. Добавьте в файл 1 три строки со словами line :
nano test4/1

line

line

line

CTRL+O

Enter

CTRL+X

### 16. Просмотрите содержимое файла 1 :
cat test4/1

### 17. Добавьте в файл 3 три строки со словами line :
nano test4/3

line

line

line

CTRL+O

Enter

CTRL+X

### 18. Просмотрите содержимое двух файлов (1 и 3) сразу :
cat test4/1 test4/3

### 19. Используя один из редакторов замените все строки в файле 1 :
nano test4/1

replaced

replaced

replaced

CTRL+O

Enter

CTRL+X


---

### Задание 2.
[Ссылка на документ](https://github.com/KaspianChi/git_bash/blob/main/bash2.txt)

### 1. Зайдите в домашнюю директорию через терминал :
cd ~

### 2. Создайте папку test3 :
mkdir test3

3. Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4
cd test3

echo -e "row1\nrow2\nrow3\nrow4" > 4

echo -e "row1\nrow2\nrow3\nrow4" > 5

echo -e "row1\nrow2\nrow3\nrow4" > 6

### 4. Найдите строку row2 в файле 5 :
grep "row2" 5

### 5. Найдите строку row в папке test3 :
grep -r "row" .

### 6. Посчитайте сколько строк с содержимым row в файле 6 :
grep -c "row" 6

### 7. Найдите файл 5 внутри папки test3 :
find . -name "5"

### 8. Используя команду find, удалите файл 5 :
find . -name "5" -exec rm {} \;

### 9. Используя команду echo, добавьте слово test в файл 4 (без сохранения содержимого) :
echo "test" > 4

### 10. Замените слово test в файле 4 на fail :
sed -i 's/test/fail/' 4

### 11. Добавьте в файл 4 слово test так, чтобы сохранилось содержимое :
echo "test" >> 4

### 12. Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе :
ps aux

### 13. Убейте процесс 666 в консоли :
kill 666

### 14. Узнайте доступность ресурса rusau.net, используя ping :
ping rusau.net

### 15. Отправьте 5 пакетов на сайт rusau.net :
ping -c 5 rusau.net

#### Для следующих двух запросов в файле Readme.md были специально проставлены дополнительные пробелы между символами "//" и после символа "@", чтобы форматирование выглядело единообразным. В файле решения таких пробелов нет.

### 16. Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https:/ /petstore.swagger.io/ :
curl -X GET "https:/ /petstore.swagger.io/v2/pet/findByStatus?status=available"

### 17. Используя POST и команду curl, создайте нового пользователя на https:/ /petstore.swagger.io/
curl -X POST "https:/ /petstore.swagger.io/v2/user" -H "accept: application/json" -H "Content-Type: application/json" -d '{"username": "testuser", "email": "test@ example.com"}'
