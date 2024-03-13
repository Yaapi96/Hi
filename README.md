## Предысловия

В этой практической работе, я познакомился с основными и самыми важными командами Git (git init, git add, git commit, git status), научился работать с локальными и удалёнными репозиториями, а также отправлять изменения из локального репозитория в удалённый и много другое.
_В своей работе я использовал командный кроцессор Bash._ 
1. Создание учетной записи GIt:
   * Задал имя пользователя и адрес электронной почты:
      
      ```
      git config --global user.name "DanielNotes"
      git config --global user.email "danilviskunov883@gmail.com"
      ```
2. Создание локального репозитория Git:
   * Создал локальный репозиторий:
   
      ```
      git init
      ```
3. Создание текстового документа:
    ```
    echo. > MyNameIs.txt
    ```
4. Добавление первого абзаца в текстовый документ:
    ```
    echo My Name Is Daniel >> MyNameIs.txt
    ```
    * Добавление изменения в индекс:
      
    ```
    git add MyNameIs.txt
    ```
    * Коммит:
      
    ```
    git commit -m "Первый абзац"
    ```

5. Просмотрел статус текущего репозитория:
    ```
    git status
    ```
6. Добавление еще одного файла:
    ```
    echo. > newf.txt
    ```
7. Создание коммита:
    ```
    git commit -m "Created news.txt"
    ```
8. Посмотр протокола коммитов:
    ```
    git log
    ```
9. Посмотр изменения в файле по сравнению с последним коммитом:
    ```
    git diff
    ```
10. Очищение изменения относительно последнего коммита из файла:
    ```
    git checkout -- newf2.txt
    ```
11. Посмотр существующих веток:
    ```
    git branch
    ```
12. Создание новой ветки:
    ```
    git branch newbranch
    ```
13. Переключение на новую ветку:
    ```
    git checkout newbranch
    ```
14. Создание новой ветку и переключение на неё одним действием:
    ```
    git checkout -b newbranch2
    ```
15. Удаление ветки:
    ```
    git branch -d newbranch2
    ```
17. Добавление merge изменения из указанной ветки в текущую:
    ```
    git checkout newbranch
    git merge master
    ```
18. Создание ребазирования *rebase* текущей ветки:
    ```
    git rebase master
    ```
18. Удаление ветки:
    ```
    git branch -d newbranch
    ```
19. Пропустил текущий конфликтный коммит и перешел к следующему:
    ```
    git rebase --skip
    ```
20. Отправление изменения из локального репозитория для указанной ветки в удаленный (дистанционный):
    ```
    git remote add origin https://github.com/zzzatoox/gitcommands.git
    git push origin master
    ```
21. Присвоение изменения из репозитория, для которого были созданы удаленные ветки по умолчанию:
    ```
    git pull origin master
    ```
22. Присвоение изменения удаленной ветки из репозитория основной ветки по умолчанию:
    ```
    git checkout -b feature-branch
    echo. > another2.txt
    git add another2.txt
    git commit -m "еще один файл сорянчик"
    git push origin feature-branch
    git pull origin feature-branch:master
    ```
23. Клонирование репозитория:
    ```
    git clone https://github.com/zzzatoox/gitcommands.git
    ```
