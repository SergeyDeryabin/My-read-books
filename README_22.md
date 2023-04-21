### Сорок(и более) штрихов о прочитанных(переведённых) книгах. 
### Штрих двадцать второй. 2017 год.

# Гийом Лазарь, Робин Пенеа. Мастеринг Qt 5. Мастерская разработка приложений: написание краткого, устойчивого и повторно используемого кода с использованием библиотеки Qt 5.
## (Guillaume Lazar, Robin Penea. Mastering Qt 5. Master application development by writing succinct, robust, and reusable code with Qt 5. ISBN 978-1-78646-712-6, Copyright © 2016 Packt Publishing)
 
p.s.

# Выдержка из книги:

## Предисловие

Язык C++ - мощный язык. Вместе с библиотекой QT в ваших руках имеется межплатформенный фреймворк, которые соединяют производительность и простоту использования. QT - обширный фреймворк, который предоставляет инструменты во многих областях (GUI-интерфейс, потоки, сети и т.д.). Спустя 25 лет после его рождения, фреймворк QT продолжает развиваться и расти с каждым выпуском.

Эта книга стремится научить вас, как выжать лучшее из совместного использования библиотеки QT и новых дополнений языка C++14 (лямбды(lambdas), умные указатели(smart pointers), классы Enum и т.д.). Вместе эти две технологии приносят вам безопасную и мощную копилку инструментов разработки. Всюду по книге мы пытаемся подчеркнуть чистую «архитектуру, которая позволяет вам создавать и поддерживать свое приложение в сложной среде.
Каждая глава основывается на проекте-примере, который является базисом всего обсуждения. Вот некоторые штрихи о том, что мы увидим в этой книге:
- Раскроем qmake-секреты
- Сделаем глубокое погружение в архитектуру модель/вид(model/view  architecture) и научитесь создавать сложное приложение по этому шаблону
- Изучим QML-язык и Qt Quick-приложения в мобильных устройствах
- Разработаем Qt 3D-компоненты, используя QML-язык и язык JavaScript
- Покажем, как разработать плагины(plugins) и SDK-наборы, используя пакет QT
- Раскроем технологии многопоточности, предоставленные пакетом QT
- Создадим IPC-механизм, используя сокеты
- Сериализуем данные, используя форматы XML, JSON и двоичный форматы

Мы охватим все эти темы и очень, намного больше.
Обратите внимание на то, что вы можете посмотреть главу 14 "Qt-шляпа с советами и приемами", каждый раз, когда вы пожелаете получить некоторые сладости разработки и увидеть некоторые фрагменты кода, которые могли бы сделать вашу разработку более радостной.
И самое главное, весело проводите время при написании Qt-приложений!

## Для кого предназначена эта книга?

Эта книга обращена к разработчикам и программистам, которые хотели бы создать приложение на базе GUI-интерфейса. Вы должны свободно владеть языком C++ и объектно-ориентированной парадигмой. Знание пакета QT рекомендуется, но необязательно.
 
## Что рассматривает эта книга?

**Глава 1 "Окунитесь немного в пакет Qt"** выкладывает фундаментальные принципы пакета QT и обновляет вашу память todo-приложением. В этой главе рассматривается структура Qt-проекта, использование проектировщика, основные принципы механизма сигналов и слотов, и представлены новые функции языка C++14.

**Глава 2 "Исследование секретов утилиты QMake"** производит глубокое погружение в сердце системы Qt-компиляции: утилита qmake. Эта глава поможет вам понять, как она работает, как использовать ее, и как вы можете структурировать Qt-приложение с платформо-зависимым(специфичным для платформы) кодом, проектируя приложение системного мониторинга.

**Глава 3 "Разделение проекта на части и управление кодом"** анализирует Qt-архитектуру модель/вид(model/view architecture) и то, как проект может быть организован при разработке пользовательской библиотеки с логикой ядра приложения. Пример проекта - приложение персистентной галереи.

**Глава 4 "Покорение настольного UI-интерфейса"** изучает перспективу использования UI-интерфейса и Qt-архитектуры модель/вид с Qt Widget-приложением с виджетами, зависящим от библиотеки, завершенной в предыдущей главе.

**Глава 5 "Управление мобильным UI-интерфейсом"** добавляет недостающую часть приложения галереи с мобильной версией (Android и iOS); глава рассматривает ее реализацию с использованием языка QML, Qt Quick-контролов (визуальных элементов управления) и взаимодействия между кодом на языках QML и C++.

**Глава 6 "Даже Qt заслуживает дольки устройства Raspberry Pi"** продолжает дорогу с Qt Quick-приложением с Qt 3D-перспективой. В этой главе рассматривается, как создать игру с 3D-змеей, предназначенную для устройства Raspberry Pi.

**Глава 7 "Подключение сторонних библиотек без головной боли"** касается того, как сторонняя библиотека может быть интегрирована в Qt-проект. Библиотека «OpenCV будет интегрирована с приложением фильтрации изображений, которая также предоставляет специализированный внешний дополнительный модуль(плагин) к проектировщику QDesigner.

**Глава 8 "Анимации - живо, живо!"** расширяет приложение фильтрации изображений, добавляя анимации и возможность распределять специализированный SDK, чтобы позволить другим разработчикам добавлять свои собственные фильтры.

**Глава 9 "Сохранение здравомыслия с многопоточностью"** исследует возможности многопоточности, предоставленные пакетом Qt, создавая многопоточное приложение рисования фрактала Мандельброта(Mandelbrot).

**Глава 10 "Требуется IPC-механизм? Заставьте своих фаворитов работать"** расширяет приложение фрактала Мандельброта(Mandelbrot), перемещая вычисление в другие процессы и управляя коммуникацией между ними, используя сокеты.

**Глава 11 "Повеселимся с сериализацией"** касается множества форматов сериализации(JSON, XML и двоичный форматы) в приложении драм-машины, в котором вы можете записать и загрузить зацикленные звуковые дорожки(звуковые лупы; sound loops).

**Глава 12 "Вы не должны пропустить фреймворк QTest"** добавляет тесты к приложению drum-машины и обучает тому, как может использоваться фреймворк QTest, чтобы сделать единичные тесты, сравнительное тестирование производительности и моделирование событий GUI-интерфейса.

**Глава 13 "Все упаковано и готово к развертыванию на устройствах"** дает понимание того, как упаковать приложение для всех настольных ОС (Windows, Linux и Mac OS) и мобильных платформ(Android и iOS).

**Глава 14 "Qt-шляпа с советами и приемами"** накопила некоторые советы и приемы, чтобы разработка с использованием пакета Qt проходила с удовольствием. Она показывает, как управлять сеансами в IDE-среде разработки Qt Creator, полезные сочетания клавиш быстрого вызова в IDE-среде разработки Qt Creator, как вы можете настроить журналирование, сохранить его на диск, и многое другое.
 
# Что потребуется для работы с книгой?

Весь код в этой книге может быть скомпилирован и запущен из IDE-среды разработки Qt Creator, использующей пакет Qt 5.7. Вы можете сделать это в своей предпочтительной ОС: Windows, Linux или Mac OS.
В мобильно-специфичных главах код выполняется на устройствах с ОС или Android или iOS, но это не обязательно (может быть достаточно запустить симулятор/эмулятор).
**Глава 6 "Даже QT заслуживает дольки устройства Raspberry Pi"** предлагает создать приложение, работающее на устройстве Raspberry Pi. Несмотря на то, что очень забавно, если мы сможем выполнить приложение на настоящем устройстве Raspberry Pi, но для того, чтобы завершить главу, нет необходимости иметь устройство.
 
## Книга:
https://www.packtpub.com/product/mastering-qt-5/9781786467126

## Загрузка кода примеров для этой книги:
https://github.com/PacktPublishing/Mastering-Qt-5

## Загрузка цветных изображений для этой книги:
Нет.