# **Инструкция по работе с Git**

## Вставка изображений

Для того чтобы втавить рисунок необходимо:

1 скопировать картинку в репозиторий

2 создать в репозитории файл .gitignore (скрытый файл)

3 закоммитить файл .gitignore

4 перенести в него файл, указав путь (если он лежит в другой папке)

5 вставить картинку в текст

Примечание: в начале строки восклицательный знак, затем в квадратных скобках указывается текст, который будет видно на месте картинки, если она не будет найдена программой; а в круглых скобках указываем название файла с расширением и путь к нему

![Flowers](Flowers.jpg)

## Инициализация репозитория

Для инициализации (создания) репозитория используется команда :

    git init

## Проверка состояния репозитория

Чтобы проверить текущеее состояние репозитория используется команда

    git status

## Добавление в индекс

Для добавления текущего содержимого (измененного) файла в индекс используется команда

    git add

## Фиксация изменений
Для фиксации в коммите изменений используется команда

     git commit

## Журнал изменений

Чтобы посмотреть историю коммитов используют команду

    git log - для просмотра подробной истории

    git log --oneline - для вывода краткой истории

## Посмотреть разницу между текущим и сохраненным коммитами
Чтобы посмотреть изменения, которые происходили с коммитами используют команду

    git diff

## Переключение между версиями

Для того чтобы перейти в нужный коммит или ветку используется команда 

    git checkout

## Ветвление

_**Ветка**_ - это последовательность коммитов.

Преимущество веток в их независимости. Можно вносить изменения в файлы в одной ветке и они накак не скажутся на файлах в другой ветке

### Использование веток

* ветки нужны чтобы разные программисты могли вести работу над проектом одновременно не мешая друг другу
* ветки используются для тестирования экспериментальных функций: если тестирование прошло успешно, изменение с экспериментальной ветки переносится на основную, а если нет - новую ветку можно просто удалить

С точки зрения логики, ветка - это последовательность коммитов; с точки зрения внутренней реализации Git, ветка - это ссылка на последний коммит в этой ветке

### Создание новой ветки

Для создания новой ветки используется команда

    git branch <branch_name>

Для того, чтобы создать новую ветку и сразу на нее перейти можно использовать команду

    git branch -b <branch_name>
    
### Просмотр списка веток

Можно использовать несколько команд для того, чтобы посмотреть список веток и их состояние.

Команды:

    git branch
выводит список локальных веток

    git log --graph
показывает взаимосвязи коммитов 

    git log --oneline --graph --all
показывает взаимосвязи всех коммитов кратко

### Слияние веток

Слияние веток - это перенос изменений с одной ветки на другую.

Для слияния веток используется команда

    git merge <branch_name>
    
### Удаление ветки

Для удаления ветки используется команда

    git branch -d <branch_name>

Нельзя удалить ветку, в которой находишься, поэтому прежде чем удалять ветку необходимо перейти с нее на другую ветку.

## Удаленные репозитории

Удаленный репозиторий - это версии проекта, сохраненные на удаленном сервере.
