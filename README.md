### KosultantPlusTask
````
test task from Konsultant Plus Co.
````
### Предназначение
````
Данная инструкция позволит вам запустить данный проект на своём ПК под OS Windows10 (на других ОС не проверял)
````
### Что понадобится скачать и установить для запуска проекта?
````
- копия данного проекта
- JDK 11+
- IDE (IntelliJ IDEA и т.п.)
- Maven
- Allure
- GoogleChrome и Firefox последних версий
````
### Настройки перед запуском
````
1.Скачать и утсановить IDE.
2.Скачать и установить JDK11+. Добавить в переменные среды JAVA_HOME и прописать путь до папки bin в каталоге JDK.
3.Скачать и учтановить Maven. Добавить в переменные среды M2_HOME...
4.Скачать и учтановить Allure. Добавить в переменные среды ALLURE_HOME...
5.Скачать и установить браузеры GoogleChrome и Firefox.
6.Скачать данный проект архивом (если нет архиватора скачать и установить). Распаковать архив.
7.Открыть IDE и выполнить импорт проекта.
8.Запуск тестов осуществляется командой - mvn clean test site -Dtest=SuitForTest, выполняемой в терминале IDE.
9.После выполнения тестов, в терминале, выполнить команду - allure serve ...target\allure-results (вместо ... указать путь до папки target в проекте).
После указаннйо выше команды откроется отчет в Allure.
10.
````
### Доп. задача
````
1. Что может пойти не так:
    - достаточно неприятный и геморный процес с настройкой Maven и Allure, так что выше указанная инструкция не гарантирует 100% запуска с первого раза,
но нерешимых проблем нет, все легко гуглится;
    - так же нужно выполнить корректный импорт проекта указав сборщик Maven иначе может возникнуть проблема, что IDE не будет воспринимать корректно классы;
    - тесты могут не зупуститься с первого раза из-за настроек IDE в которой дефолтно будет стоять версия JDK меньше 11;
    - разумеется без интернета тесты не будут выполняться корректно;
    - в атотестах используется кирилица, так что в pom-файл добавлены зависимости решающие этупроблему.
2. Проблемы с которыми я столнулся были учтены и более подробно описаны в файле "Errors".
````
## Доп. материалы.
````
- [settings for JDK and Maven](https://github.com/Flibberty-GEA/blog/wiki/03.a-%D0%9A%D0%B0%D0%BA-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-Maven-%D0%BD%D0%B0-Windows-10)
- [settings for Allure](https://habr.com/ru/company/sberbank/blog/358836/)