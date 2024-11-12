# ESP-Octo: Эмулятор CHIP-8 для ESP32-2432S024C с сенсорным экраном 🎮👾

![Эмулятор CHIP-8](/doc/play.png)

ESP-Octo - это потрясающий проект, который позволяет вам исследовать и создавать игры на платформе CHIP-8 на плате ESP32-2432S024C с сенсорным экраном. Этот эмулятор был разработан Джоном Эрнестом и портирован на плату ESP32-2432S024C с сенсорным экраном, чтобы создать дешевое, самодостаточное устройство, которое не требует подключения к компьютеру. 💻🔌

## Функции

- Эмулятор CHIP-8 с поддержкой оригинальных 16 инструкций и некоторых расширений SCHIP 📝
- Сенсорный интерфейс с датчиком CST820, подключенным через I2C 👆
- 320x240 пиксельный дисплей с классическим отображением CHIP-8 и четырьмя кнопками для навигации по играм и выбора режима 📱
- Поддержка игр из [архива CHIP-8](https://johnearnest.github.io/chip8Archive/) 📁
- Встроенный монитор и дизассемблер для отладки и обучения 🔧
- Небольшая и дешевая плата ESP32-2432S024C с дисплеем, аккумулятором и небольшим динамиком 💡
- Поддержка контроллера Nunchuk для Wii в качестве игрового контроллера с небольшим адаптером 🎮

## Начало работы

Чтобы получить проект, используйте `git clone --recursive`, чтобы получить необходимые подмодули. Проект использует библиотеку LovyanGFX для дисплея и библиотеку CST820 для сенсорного интерфейса. Игры хранятся на карте SD в каталоге "/chip8", а файл "chip8.txt" создается из "chip8Archive/programs.json" с помощью небольшого скрипта на Python.

Чтобы скомпилировать проект, используйте Arduino IDE или инструменты ESP-IDF. Проект также может быть установлен через https://esp.huhn.me/ с помощью предварительно скомпилированной версии.
### НЕ РАБОТАЕТ БЕЗ SD-КАРТЫ
1. Bootloader - 0x1000
2. Partitions - 0x8000
3. Firmware - 0x1000
   
## Аппаратная часть

ESP32-2432S024C - это небольшая и дешевая плата с дисплеем, и проект включает в себя аккумулятор и небольшой динамик, подключенные к соответствующим разъемам JST 1.25. Вот некоторые фотографии платы:

![Передняя левая часть](/doc/board-frontleft.jpg)
![Задняя часть](/doc/board-back.jpg)
![Задняя левая часть](/doc/board-backleft.jpg)

Для защиты компонентов необходимо изготовить корпус из 3D-печати.

## Аксессуары

Проект включает в себя поддержку контроллера Nunchuk для Wii в качестве игрового контроллера с небольшим адаптером. К сожалению, автору не удалось заставить контроллер Nunchuk работать с приведенным примером кода.

![Контроллер Nunchuk](/doc/wii-nunchuk.jpg)

## Заключение

ESP-Octo - это замечательный проект, который позволяет вам изучать архитектуру CHIP-8 и создавать собственные игры. Проект является открытым исходным кодом и может быть легко модифицирован и расширен в соответствии с вашими потребностями. Присоединяйтесь к нашему сообществу разработчиков и создавайте удивительные игры на платформе ESP32-2432S024C с сенсорным экраном. 🎮👾💻🔧👩‍💻

## Лицензия

ESP-Octo лицензирован на условиях лицензии MIT. Подробности см. в файле [LICENSE](https://github.com/huhn/esp-octo/blob/main/LICENSE).

## Благодарности

- [John Earnest](https://github.com/JohnEarnest) за оригинальный эмулятор Octo 💡
- [LovyanGFX](https://github.com/lovyan03/LovyanGFX) за библиотеку дисплея 📱
- [CST820](https://github.com/NoosaHydro/2.4inch_ESP32-2432S024.git) за библиотеку сенсорного интерфейса 👆
- [thingm](https://labs.thingm.com) за адаптер контроллера Nunchuk 🎮
- [Adafruit](https://www.adafruit.com/) за небольшой динамик 🔊
- [Sunton](https://www.sunton.com/) за плату ESP32-2432S024C 💡
- [CHIP-8 archive](https://johnearnest.github.io/chip8Archive/) за игры 🎮
