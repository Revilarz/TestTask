### KosultantPlusTask
````
test task from Konsultant Plus Co.
````
### Предназначение
````
Данная инструкция позволит вам запустить данный проект на своём ПК под OS Windows10 (на других ОС не проверял)
````
### Что понадобится скачать и установить для запуска проекта:
````
- копия данного проекта
- JDK 12
- IDE (IntelliJ IDEA и т.п.)
- Maven
- Allure
- GoogleChrome и Firefox последних версий
````
### Настройки перед запуском
````
1.Скачать и утсановить IDE.
2.Скачать и установить JDK12. Добавить в переменные среды JAVA_HOME.(подробнее в доп. материалах)
3.Скачать и учтановить Maven. Добавить в переменные среды M2_HOME.(подробнее в доп. материалах)
4.Скачать и учтановить Allure. Добавить в переменные среды ALLURE_HOME.(подробнее в доп. материалах)
5.Скачать и установить браузеры GoogleChrome и Firefox.
6.Скачать данный проект архивом (если нет архиватора скачать и установить). Распаковать архив.
Кроме архива есть альтернативнй сопособ, необходимо скачать и установить Git и командой git clone скачать проект.
7.Открыть IDE и выполнить импорт проекта.
8.Перед запуском есть возможность задать браузер(browser) и ожидаемое максимальное время открытия документа(timeout) в файле plus.properties.
9.Запуск тестов осуществляется командой - mvn clean test site -Dtest=SuitForTest, выполняемой в терминале IDE.
10.После выполнения тестов, в терминале, выполнить команду - allure serve ...target\allure-results (вместо ... указать путь до папки target в проекте).
После указаннйо выше команды откроется отчет в Allure.
11.Для десятого теста (TenthTest) реализован вывод проверяемых дат в очтет, при просомтре Allure отчета нужно будет
выбрать десятый тест, открыть его подробные свойства и кликнуть на тексты с надписью: "Дата начала действия редакций:".
````
### Доп. задача
````
1. Что может пойти не так:
    - достаточно неприятный и геморный процес с настройкой Maven и Allure, так что выше указанная инструкция не гарантирует 100% запуска с первого раза,
но нерешимых проблем нет, все легко гуглится;
    - так же нужно выполнить корректный импорт проекта указав сборщик Maven иначе может возникнуть проблема, что IDE не будет воспринимать корректно классы;
    - тесты могут не зупуститься с первого раза из-за настроек IDE в которой дефолтно будет стоять версия JDK меньше 11;
    - разумеется без интернета тесты не будут выполняться корректно;
    - в атотестах используется кирилица, так что в pom-файл добавлены зависимости решающие этупроблему;
    - при задании в файле plus.properties отличного от указанного url тесты не будут работать корректно;
    - данные тесты зависимые, что плохо, поэтому если что то не так пойдетт с одним тестов упасть
иогут и пара остальных (придать независимость тестам не проблема) это было сделаоно для максимальной простоты восприятия
каждый тест соовтсетвует пункту задания.
2. Проблемы с которыми я столнулся были учтены и более подробно описаны в файле "Errors".
````
## Доп. материалы.
````
- [settings for JDK and Maven](https://github.com/Flibberty-GEA/blog/wiki/03.a-%D0%9A%D0%B0%D0%BA-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-Maven-%D0%BD%D0%B0-Windows-10)
- [settings for Allure](https://habr.com/ru/company/sberbank/blog/358836/)
````