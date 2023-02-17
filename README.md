Copyright (C) 2022, VadRov, all right reserved.

# Модуль для работы с кнопоками на микроконтроллере stm32f4 (и не только stm32f4, и не только stm32).

Путем несложной модификации модуль возможно использовать на любых микроконтроллерах, отвечающих минимальным требованиям.

Модуль позволяет программно устранять дребезг контактов, реализует программируемый автоповтор нажатия кнопки с заданным периодом и реализует
буферизованный ввод с заданной глубиной буфера.

Выводы микроконтроллера, к которым подключаются кнопки, должны быть настроены как входы с подтяжкой по питанию. Как вариант, с использованием
внутренней подтяжки микроконтроллера pull-up, либо внешней через подтягивающий резистор, например, номиналом 10 кОм.
При нажатии кнопки должна осуществляется притяжка входа к "земле" (GND).
Для работы библиотеки требуется 1 таймер с настроенным прерыванием по обновлению.

Возможности модуля keybord:
- Поддержка до 32 кнопок, с учетом того, что на 1 кнопку выделяется 1 вывод микроконтроллера,
настроенный на вход с подтяжкой по питанию.
- Доступна настройка фильтра устранения дребезга.
- Доступен буфер состояний кнопок с настраиваемой глубиной.
- Доступна настройка периодов задержки до первого автоповтора нажатия кнопок и последующих автоповторов.
- Доступно добавление кнопок для опроса посредством вызова соответствующей функции.
- Доступна установка статусов кнопки: "активна" - участвует в опросе, "пассивна" - не участвует в опросе.
- Доступен опрос статуса кнопки (активна либо пассивна).

В проекте, созданном в среде STM32CubeIDE, реализован пример работы с кнопками на микроконтроллере stm32f401ccu6 с использованием 
модуля keyboard.

В видео подробно рассказано об использовании модуля и приведен пример построения проекта в среде STM32CubeIDE:
 [![Watch the video](https://img.youtube.com/vi/e-w5HS75neg/maxresdefault.jpg)](https://youtu.be/e-w5HS75neg)

Автор: **VadRov**

Контакты: [Youtube](https://www.youtube.com/@VadRov) [Дзен](https://dzen.ru/vadrov) [VK](https://vk.com/vadrov) [Telegram](https://t.me/vadrov_channel)

Поддержать автора: [donate.qiwi](https://donate.qiwi.com/payin/VadRov)  [donate.yoomoney](https://yoomoney.ru/to/4100117522443917)
