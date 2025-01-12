# Туториал по работе с Git (Изменения от Двирского Николая)

## Начало работы

Для начала работы, необходимо инициализировать сам Git

Для его инициализации введите команду 

```
  git init
```

## Добавление файла

Для добавления файла в Git необходимо воспользоваться командой 

```
git add название файла
```
# Иструкция по работе с GIT
## Введение
**Определения**  

*__Git__ - это программа, предназначенная для сохранения и управления версиями кода в виде текста, усттановленный непосредственно на ПК. Самая популярная система контроля версий. Создатель - Линус Торвальдс*  

GitHub - это интернет сервис от Microsoft, который позволяет удалённо хранить код и производить контроль версий

*coommit (англ.) - зафиксировать, сохранить*

**Назначение GIT:**
* хранить версии проекта
* возможность возвращаться к старой версии  



## Установка GIT и регистрация
**Для работы необходимо установить следующее ПО:**
1. Git
2. VS Code 
3. Ввести свои идентификационные данные: логин, адрес эл.почты
со
```
git config -global user.email название почты
git config -global user.name имя
```
4. Открыть терминал и с помощью команды проверить актуальность версии Git и наличие компонентов
```
git --version
```
Очистить терминал от не нужных записей 
clear
Вызов и перемещение ранее применяемых команд производится с помощью кнопок вверх/вниз
Продление команды или названия файла с помощью кнопки Tab

## Начало работы в GIT
1. Создать рабочую папку для проекта
2. Создать из папки репозиторий (отслеживаемый системой объект)  
```
git init
```
initialization (англ.) - иницианализация
3. Проверить состояние репозитория
git status  
4. Создать в Git файл, заменяя пробелы нижним подчёркиванием. Имя файла писать латинским буквами с указа расширения

имя_файла.txt

## Сохранение версий, создание папок/веток и перемещение между ними  

Сохранить файл
```
git add название_файл.расширение
git commit -m "название сохранения"
```
Вывести список сохранения
```
git log
```
Вывести спосок сохарнений в виде графика
```
git --graph
```
Перейти на другое сохранение (коммит). Достаточно ввести 4 символа.
```
git checkout 2a55...
```
Перейти в другой репозиторий (папку). Cd (англ.) - change direct
```
сd
```
Посмотреть разницу между текущим и предыдущим коммитом
```
git diff
```

## Ветвление
*branche (англ.) - ветка*

Вывести информацию о ветках: наличие, позиция
```
git branche
```
**Объединение веток**
1. Перейти в главную ветку master
``` 
gti checkout brance название ветки
```
2. Указать ветку с которой перести код
```
git merge название ветки
```
Удаление ветки
```
git brance -d название ветки
```

## Работа с удалённым репозиторием
1. Проиходим регистрацию GitHub.com
2. Связываем локальный репозиторий с удалённым с помощью 3-х команд



## Полезная информация и примечания
Тренажор по Git находится на сайте LearnGitBranching

В репозитории не принято хранить большие файлы (видео, картинки) поэтому их хранят локально, перечень файлов указывают в специальном файле *.gitignore*. Название пишется полностью с расширением. Файл с названиями исключений также необходимо добавить в отслеживаемые
```
git add .gitignore
git commit -m "Название файла.расширение"
```
**Порядок действий при совместной разработке с помощью совместного репозитория**
1. Заходим в чужой репозиторий на GitHub
2. Копируем проект с чужого удалённого репозитория в свой удалённый репозиторий с помощью нажатия кнопки Fork
3. Клонируем файл в локальый репозиторий (clone)
4. Создаём отдельную ветку, где будем редактировать чужой файл
5. Отправляем изменения (push) в свой удалённый репозиторий
6. В окне удалённого репозитория предлагаем изменения с помощью нажатия кнопки pull request


