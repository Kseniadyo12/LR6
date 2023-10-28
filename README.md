# LR6
Лабораторная работа №6

Список команд, которые были использованы в лабораторной работе:

- `git config --global user.name "Your Name"`  # указать имя, которым будут подписаны коммиты

- `git config --global user.email "e@w.com"`  # указать эл.почту, которая будет в описании коммитера

- `git clone`  # показать состояние репозитория (отслеживаемые, изменённые, новые файлы и пр.)

- `cd`  # используется для смены текущего каталога

- `git pull`  # влить изменения с удалённого репозитория

- `git log`  # показать коммиты в указанной ветке

    с параметрами `-p -2` позволяет увидеть два последних коммита

- `git checkout new_branch`  # перейти в указанную ветку

- `git merge hotfix`  # влить в ветку, в которой находимся, данные из ветки hotfix

- `git status`  # просмотреть статус нужного репозитория

- `git add`  # добавить файл

- `git commit -m`  # зафиксировать в коммите проиндексированные изменения (закоммитить), добавить сообщение

- `git branch -d hotfix`  # удалить ветку hotfix (используется, если её изменения уже влиты в главную ветку)

- `echo текст > файл` # создать файл с текстом

- `git reset HEAD~1` # выполнить откат коммита на одно изменение

- `git branch new_branch`  # создать новую ветку с указанным именем

- `git log --date=format:'%D' --pretty=format:"%h - %cd, %cn : %s"` позволяет вывести историю операций в форматированном виде, где

    `%h` - сокращенный хэш коммита

    `%cd` - дата коммита

    `%cn` - имя коммитера
 
    `%s` - содержание


Ход работы

В личное хранилище на github был скопирован репозиторий с помощью Fork.

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/1.png)
![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/2.png)

Был скачан Git и введены имя пользователя и почта.
После этого была сделана локальная копия репозитория с помощью `git clone`

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/3.png)

В GitHub был добавлен файл New file. 
Переходим в скопированный репозиторий с помощью `cd`, далее вызывается команда `git pull`, которая подгружает в локальный реапозиторий изменения, внесенные на GitHub.

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/4.png)

Дальнейшая работа будет происходить локально

С помощью `git log` можно посмотреть последние изменения

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/5.png)

Использование `git log -p -2` позволяет увидеть два последних коммита

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/6.png)

Далее переходим в ветку **branch1** с помощью `git checkout`

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/7.png)

Теперь можно посмотреть лог в данной ветке

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/8.png)
![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/9.png)

Чтобы объединить ветки, используется команда `git merge`

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/10.png)

При попытке выполнить команду замечаем конфликт. 
Узнать состояние и увидеть возможные ошибки позволяет команда `git status`. Выполнив ее, понимаем причину проблемы - присутствуют несоединенные пути. 
Разрешить конфликт можно добавив файл mergefile.txt командой `git add`. После исправления конфликта еще раз проверяем статус проекта.

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/11.png)

Теперь можно закоммитить изменения командой `git commit -m`, где -m используется для добавления комментария в консоли. 
Ненужную ветку удаляем командой `git branch -d`

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/12.png)

Вносим дальнейшие изменения следующим образом: 
- `echo текст > файл` создает файл с текстом
- `git add файл` добавляет созданный файл
- `git commit -m "изменение n"` коммитит изменение с комментарием

Этот порядок действий мы применяем три раза (создаем 3 файла).

>первый файл

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/13.png)

>второй файл + проверка

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/14.png)
![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/15.png)

>третий файл

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/16.png)

Выводим все изменения в логе

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/17.png)

`git reset HEAD~1` позволяет выполнить откат коммита на одно изменение.

Выполнив откат, еще раз проверим лог - остануться только _Изменение 2_ и _Изменение 1_.

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/18.png)

Для выполнения отчета создается ветка record с помощью команды `git branch record`

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/19.png)

`git log --date=format:'%D' --pretty=format:"%h - %cd, %cn : %s"` позволяет вывести историю операций в форматированном виде, где

`%h` - сокращенный хэш коммита

`%cd` - дата коммита

`%cn` - имя коммитера

`%s` - содержание

![](https://github.com/Kseniadyo12/LR6/blob/record/Screenshots/20.png)

