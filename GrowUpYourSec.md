# Чек-лист по выстраиванию безопасности за пару дней

## Сокращаем поверхность атаки
Сканируем свои публичные подсети
* Все TCP `sudo nmap -n -Pn -T4 -p 1-65535 192.168.1.1/24`
* Выборочно UDP `sudo nmap -n -Pn –sU -F 192.168.1.1/24`
* IP scan `sudo nmap -n -Pn –sO 192.168.1.1/24`

Используем https://www.shodan.io
* org:"Open Joint-stock company XXX"

Ограничиваем доступ
* ACL для непубличных ресурсов
* Ограничить удаленный доступ (VPN, Citrix, VDI)
* Наивные проверки (например, по user-agent)
* Ограничение по GeoIP
* Ограничение внешних контрагентов (например, техподдержки интернет провайдера)

Сокращаем доступную информацию
* Убираем баннеры сервисов, web-серверов, CMS и прочего (но не занижаем)
* Сетевые протоколы ограничиваем
* [Методы HTTP](https://developer.mozilla.org/ru/docs/Web/HTTP/Methods) ограничиваем   
([Test HTTP Method](https://github.com/OWASP/wstg/blob/master/document/4-Web_Application_Security_Testing/02-Configuration_and_Deployment_Management_Testing/06-Test_HTTP_Methods.md))
* Открытые файловые шары, доступные директории убираем ([dirsearch](https://github.com/maurosoria/dirsearch), [Google Dorks](https://www.exploit-db.com/google-hacking-database))
* Закрываем Swagger

Контролируем утечки (ищем `домены, логины, e-mail-адреса`)
* Публичные хранилища кода ([github](https://github.com), [gitlab](https://gitlab.com))
* Онлайн-буферы обмена ([pastebin](https://pastebin.com))
* Онлайн-доски ([trello](https://trello.com))
* Внутренние ресурсы

## Убираем очевидные дыры
* Контролируем доступы
* Меняем дефолтные УЗ всех внешних сервисов (лучше лочим)
* Подключаем 2-факторную аутентификацию
* Запуск внешних сервисов под УЗ с ограниченными правами
* Все пароли внепланово обновить
> *Составь пароль по антипаттерну:*  
> Начни с 2-х спецсимволов (без `! . _ - @`)  
> Цифры в середину (лучше без `1` и `2`)  
> Прописную букву не в начало  

Обновляем публичное ПО
* Смотрим наличие критичных (CVE > 6-7) недостатков (https://vulners.com, https://cve.mitre.org, https://nvd.nist.gov)
* Особенное внимание системам, где есть публичные эксплоиты (https://www.exploit-db.com)
* Если нельзя обновиться – смотрим описание и снижаем риск компенсационными мерами (см. также [виртуальный патчинг](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Virtual_Patching_Cheat_Sheet.md))

Изучаем и применяем основы безопасной разработки
* [OWASP Top 10](https://owasp.org/Top10/)
* [OWASP API Security Top 10](https://github.com/OWASP/API-Security)
* [OWASP Mobile Top 10](https://github.com/OWASP/www-project-mobile-top-10/blob/master/2016-risks/index.md)

## Конролируем зависимости
Отслеживаем protestware
* [CTO Club list](https://docs.google.com/spreadsheets/d/1H3xPB4PgWeFcHjZ7NOPtrcya_Ua4jUolWm-7z9-jSpQ/htmlview?pru=AAABf7z88MA*ITSp0EBrKinw0LjFWZ9tzQ#gid=2074850979)
* [Protestware-list](https://github.com/open-source-peace/protestware-list)
* Habr и другие тематические источники

Избавляемся от внешних скриптов
* Сокращаем GTM, метрики, чатики, счетчики и пр.
* Ограничиваем используемые скрипты (например, [настроить ограничения для Я.Метрики](https://yandex.com/support/metrica/general/confidential-data.html?lang=ru))

Вводим карантин для зависимостей
* Не бежим за свежими обновлениями (задержка 1-2 недели)
* Наивные проверки (условия на таймзону, geoIP)
* Тестовый запуск в контейнере
* Учитываем транзитивные зависимости

## Боремся с социальной инженерией
Технические меры
* Права доступа – минимальные для работы
* Почтовый «маркер» для внешних писем с вложениями  
`Это письмо получен от внешнего отправителя, не открывайте вложения`
* По умолчанию не грузим информацию из внешних источников

Обучение с подкреплением
* Провести тестовую рассылку  
`Исполняемое вложение отстукивается (hostname машины) на  заранее подготовленный сервер`  
`Легенда письма – повышение ЗП`
* Провести повторное обучение с теми, кто открыл вложение



