# Практическая работа GIT
<p align="center">
      <img src="https://upload.wikimedia.org/wikipedia/commons/e/e0/Git-logo.svg" width="450">
</p>

***Задать имя пользователя и адрес электронной почты***

```
git config --global user.name "mqwxz"
git config --global user.email "************@gmail.com"
```


✅ ***1. Создать учетную запись на ресурсе github.com***

✅ ***2. Создать на ресурсе github.com репозиторий для выполнения
практической работы.***

✅ ***3. Создать папку для работы с Git.***
```
$ cd D:\
$ mkdir git30
$ git init 
```

✅ ***4. Создать локальный репозиторий в текущей папке.***
```
$ cd git30
$ git init
```

✅ ***5. Добавьте туда пустой текстовый документ.***
```
$ echo "">> something.txt
$ git add something.txt
```

✅ ***6. Сформируйте этот документ, создавая commit для каждого абзаца, не
менее 5 абзацев.***
```
$ echo "1 абзац" >> something.txt
$ git add something.txt
$ git commit -m "1st paragraph"

$ echo "2 абзац" >> something.txt
$ git add something.txt
$ git commit -m "2nd paragraph"

$ echo "3 абзац" >> something.txt
$ git add something.txt
$ git commit -m "3rd paragraph"

$ echo "4 абзац" >> something.txt
$ git add something.txt
$ git commit -m "4th paragraph"

$ echo "5 абзац" >> something.txt
$ git add something.txt
$ git commit -m "5th paragraph"
```

✅ ***7. Посмотреть статус текущего репозитория.***
```
$ git status
```

✅ ***8. Добавить файл.***
```
$ echo >> file.txt 
$ git add file.txt
```

✅ ***9. Создать коммит, указать для него комментарий.***
```
$ git commit -m "added another text file"
```

✅ ***10. Посмотреть протокол коммитов.***
```
$ git log -p
```

✅ ***11. Посмотреть изменения в файле по сравнению с последним
коммитом.***
```
$ git diff
```

✅ ***12. Убрать изменения относительно последнего коммита из файла.***
```
$ git checkout -- something.txt
```

✅ ***13. Просмотреть существующие ветки.***
```
$ git branch
```

✅ ***14. Создать новую ветку.***
```
$ git branch new_branch_name
```

✅ ***15. Переключиться на другую ветку.***
```
$ git checkout new_branch_name
```

✅ ***16. Создать новую ветку и сразу же переключиться на нее.***
```
$ git checkout -b sec_branch
```

✅ ***17. Удалить ветку.***
```
$ git branch -D new_branch_name
```

✅ ***18. Добавить (merge) изменения из указанной ветки в текущую.***
```
$ git merge master
```

✅ ***19-23. Создать конфликт.***
```
$ git checkout master
$ echo "temp" >> file.txt
$ git add file.txt
$ git commit -m "temp"

$ echo "different content" > file.txt
$ git commit -m "edit file.txt"

$ echo "new content" >> file.txt
$ git commit -am "new content file.txt"
$ git merge sec_branch

$ git status
```

✅ ***20-24. Посмотреть в каких файлах есть конфликты.***
```
$ cat file.txt
```
```
<<<<<<< HEAD

temp
temp1
new content
=======
different content
>>>>>>> sec_branch
```

✅ ***21. Устранить конфликты.***
Удаление всех разделителей конфликта при редактировании.
```
$ git commit -m "deleted conflicts from file.txt"
```

✅ ***22. Переключиться на указанный коммит.***
```
$ git checkout b71e186
```

✅ ***23. Сделать ребазирование (rebase) текущей ветки.***
```
$ git rebase master
```

✅ ***24. Удалить ветку.***
```
$ git branch -D sec_branch
```

✅ ***25. Пропустить текущий конфликтный коммит и перейти к следующему.***
- Его нет.

✅ ***26. Отправить изменения из локального репозитория для указанной
ветки в удаленный (дистанционный).***
```
$ git remote add origin https://github.com/mqwxz/git30.git
$ git push origin master
```

✅ ***27.Забрать изменения из репозитория, для которого
были созданы удаленные ветки по умолчанию.***
```
$ git pull origin master
```

✅ ***28. Забрать изменения удаленной ветки из репозитория основной ветки
по умолчанию.***
```
$ echo "sample text" >> file1.txt
$ git add file1.txt
$ git commit -m "added file1.txt"
$ git push origin th_branch
$ git pull origin th_branch:master
```

✅ ***29. Создать копию репозитория.***
```
$ git clone https://github.com/mqwxz/git30.git
```
