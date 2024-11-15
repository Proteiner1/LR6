# LR6
Лабораторная работа №6

# Отчет по лабораторной работе №6
## Тема: Система контроля версий

## Цель лабораторной работы
Изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и
удаленным репозиторием. 

## Порядок выполнения работы
В ходе выполнения работы были выполнены следующие шаги:

### Шаг 1: Создание аккаунта на GitHub
Зарегистрирован аккаунт на сайте GitHub.

### Шаг 2: Форк репозитория
Форкнут репозиторий с заданием: [https://github.com/Kurtyanik/LR6](https://github.com/Kurtyanik/LR6).

![Скриншот форка репозитория](https://i.postimg.cc/9XRPS2fp/image.png)

### Шаг 3: Установка Git
Установлен Git с сайта [https://git-scm.com/](https://git-scm.com/).

### Шаг 4: Настройка Git
Настроен клиент Git с помощью следующих команд:

```bash
git config --global user.name "Группа Фамилия И.О."
git config --global user.email "ваш_емейл@example.com"
```
![Скриншот настройки клиента](https://i.postimg.cc/3xnDNfRN/image.png)

### Шаг 5: Клонирование репозитория

```bash
git clone https://github.com/Kurtyanik/LR6
```
![Скриншот клонирования репозитория](https://i.postimg.cc/L8X8C994/image.png)

### Шаг 6: Добавление файла через GitHub и подтягивание изменений
Добавлен файл через веб-интерфейс GitHub и изменения подтянуты локально:

```bash
git pull
```
![Скриншот добавления файла](https://i.postimg.cc/mDxZg7Qh/image.png)

### Шаг 7: Получение истории операций
Получена история операций для каждой ветки:

```bash
git log --oneline --all
```
![Скриншот истории операций для каждой ветки](https://i.postimg.cc/L6sSRxrN/image.png)

### Шаг 8: Просмотр последних изменений
Посмотрены последние изменения:

```bash
git log -p -1
```
![Скриншот просмотра последних изменений](https://i.postimg.cc/gJcSRTy7/image.png)

### Шаг 9: Слияние ветки и разрешение конфликта
Создана и слита ветка feature в master, конфликтов не возникло:

```bash
git checkout -b feature
# Внесены изменения
git add .
git commit -m "Изменения в ветке feature"
git checkout master
git merge feature
```
![Скриншот слияния веток](https://i.postimg.cc/MHQFKjmZ/image.png)

### Шаг 10: Удаление побочной ветки
Удалена ветка feature после слияния:

```bash
git branch -d feature
```

### Шаг 11: Сделаны несколько коммитов с комментариями
Внесены изменения в файл example.txt (поочерёдно добавил две строки) и сделаны коммиты:

```bash
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "добавил ещё одну строку.txt"
```
![Скриншот создания коммитов](https://i.postimg.cc/SK4k0mqz/image.png)

### Шаг 12: Откат коммита
Выполнен откат последнего коммита:

```bash
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "добавил ещё одну строку.txt"
```
![Скриншот отката коммита](https://i.postimg.cc/8c7Vd5dx/image.png)


### Шаг 13: Создание ветки для отчета
Создана ветка report для оформления отчета:

```bash
git branch report
git checkout report
```
![Скриншот создания ветки для отчёта](https://i.postimg.cc/RCYmS74m/image.png)

## Лог команд

```bash
# Настройка имени пользователя и email
git config --global user.name "4314 Немченков А. С."
git config --global user.email "Alexey.nemchenkov@gmail.com"

# Клонирование форкнутого репозитория
git clone https://github.com/Kurtyanik/LR6

# Переключение в директорию проекта
cd LR6

# Получение истории операций для всех веток
git log --oneline --all

# Просмотр последних изменений
git log -p -1

# Создание новой ветки
git branch feature

# Переключение на новую ветку
git checkout feature

# Внесение изменений, добавление их в индекс и коммит
git add example.txt
git commit -m "Добавил новую строку в example.txt"

# Переключение обратно на мастер и слияние веток
git checkout master
git merge feature

# Удаление побочной ветки после слияния
git branch -d feature

# Создание еще нескольких коммитов с комментариями
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку"

# Откат последнего коммита
git revert HEAD

# Создание ветки для отчета и переключение на нее
git branch report
git checkout report

# Получение истории операций в отформатированном виде
git log --pretty=format:"%h %ad | %s%d [%an]" --date=short

# Отправка изменений на удаленный репозиторий
git push origin report
```

### Пояснение:
Этот лог команд показывает весь процесс выполнения лабораторной работы, включая настройку Git, создание веток, коммиты, слияние, откат коммитов и отправку изменений на GitHub.

## История операций
Получим и напечатаем историю операций. Сделаем это при помощи команды:

```bash
git log --pretty=format:"%h %ad | %s%d [%an]" --date=short
```
Результат выполнения программы:
![Скриншот создания ветки для отчёта](https://i.postimg.cc/vZqkhMTs/image.png)

## Вывод
В ходе выполнения лабораторной работы были изучены основные возможности системы контроля версий Git. Получены навыки работы с локальными и удаленными репозиториями, создания и слияния веток, разрешения конфликтов и оформления отчета в README.md файле.

