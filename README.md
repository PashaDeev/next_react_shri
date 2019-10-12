# React

Скачайте и установите зависимости

При разработке использовлась

Node.js версии **12.6.0**

Для работы обязательно наличие запущенного сервера  
 [Сылка на репозиторий сервера](https://github.com/WD-man/git_server).  
 Для корректной работы тестов, не следует переназначать путь до корневой директории.  
 На сервере есть тестовый репозиторий.

---

__FIX__  
На роут `/`  были добавлены кнопки __Создать__ и __Удалить__,  
Которые добаляют и удаляют определенный тестовый репозиторий.

Для **SSR** Использовался фреймворк [Next.js](https://nextjs.org)

В качестве сервера не используется стандартный сервер nextjs, для возможности
ручного управления роутингом и перенапраавления запросов.

Для запуска Production версии приложения выполните:

`npm run start`  

По умолчанию сервер запускается на порту **8076**  
Для изменения нужно передать порт в качестве переменной окружения  

`PORT=$port npm run start`

[Ссылка](http://localhost:8077)

`/` - страница со списком всех существующих репозиториев

`/directories` - роут для страниц содеримого папок. Попытка  
 запуска без параметров приведет к ошибке, Поэтому лучше переходить  
 по ссылкам.

`/files` - роут для страниц содержимого файлов. Попытка вызова без параметров  
 также приведет к ошибке


Нет роутов к файлам по прямому пути потому что, по моему мнению эти,  
 файлы не должны индексироваться и поэтому не требуют прямых ссылок.
 
 Все результаты отображаются из **master** ветки репозитория.

## Тесты

Настройка окружения Hermione:

Для запуска тестов должен быть chrome webdriver.

`npm i selenium-standalone --global`

`selenium-standalone install`

`npm i hermione`

В отдельной вкладке терминала:

`selenium-standalone start`

Запуск gui hermione

`npm run hermione`


### Логические блоки системы

- Блок связи с сервером, для получения данных
- Блок работы с состоянием
- Блок представления, которые из себя представляет набор React компонентво

Для этого репозитория написаны интеграционные тесты с помощью пакета Hermione
