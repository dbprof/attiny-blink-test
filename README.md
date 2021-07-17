# ATTINY85 ATTINY13A BLINK TEST
Подключаем и проверяем микроконтроллеры ATtiny85 ATtiny13A с помощью Arduino NANO в среде Arduino IDE.
Для этого прошьем их при помощи Arduino NANO и помигаем зеленым светодиодом.
Собераем на макетке по схеме:

![Схема подключения](https://github.com/dbprof/attiny-blink-test/blob/main/schema.jpg)

Понадобится:
* 1х Arduino NANO - https://aliexpress.ru/item/32647196840.html
* 1х ATtiny85 - https://aliexpress.ru/item/32952262601.html - 117р.
* 1х ATTINY13A - https://aliexpress.ru/item/33017673622.html - 42р.
* 2х Breadboard мини - https://aliexpress.ru/item/4000515189300.html

1. Подготовка Arduino NANO:
* запускаем Arduino IDE
* открываем скетч ArduinoISP (Файл>Примеры>11.ArduinoISP)
* подключаем Ардуино к компьютеру и загружаем в нее скетч

2. Добавляем возможность работы среды Arduino IDE с микроконтроллерами ATtiny85:
* открываем меню Файл>Настройки и в появившемся окне нажимаем кнопку рядом с полем ввода дополнительных ссылок для Менеджера плат
* вставляем в поле "Дополнительные ссылки для Менеджера плат:" ссылку "http://drazzy.com/package_drazzy.com_index.json" и нажимаем ОК
* в случае ATTINY13A ссылка: "https://mcudude.github.io/MicroCore/package_MCUdude_MicroCore_index.json"
* открываем Инструменты>Плата>Менеджер плат и в строке поиска набираем "ATtiny", устанавливаем "ATtinyCore by SpenceKonde"
* в случае ATTINY13A открываем Инструменты>Плата>Менеджер плат и в строке поиска набираем "ATtiny", устанавливаем "MicroCore by MCUdude"

3. Подключаем ATtiny к Arduino NANO и прошиваем:
* после этого выбираем Инструменты>Плата>ATTinyCore>"ATtiny25/45/85 (No bootloader)"
* в случае ATTINY13A Инструменты>Плата>MicroCore>"ATtiny13"
* также выбираем Инструменты>Программатор>"Arduino as ISP (ATTinyCore)"
* нажимаем "Записать Загрузчик" (Будет выдана ошибка, но это необходимо для выставления частоты)
* далее выбираем Скетч>"Загрузить через программатор"

Если все успешно, то светодиод начинает мигать - 3 секунды светит, 3 секунды пауза.

Видео по сборке:
[![Видео](https://github.com/dbprof/attiny-blink-test/blob/main/video2.png)](https://youtu.be/_aGBYGrZLdw)
