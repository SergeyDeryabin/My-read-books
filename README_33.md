### Пятьдесят штрихов о прочитанных(переведённых) книгах. 
### Штрих тридцать третий. 2020 год.

# Павел Страхов, Витольд Визота, Лоренц Хаас. Программирование игр с использованием Qt 5. Руководство для начинающих. Вторая редакция. Создайте удивительные игры с использованием Qt 5, C++ и Qt Quick пер.
## (Pavel Strakhov, Witold Wysota, Lorenz Haas. Game Programming Using Qt 5 Beginner's Guide. Second Edition. Create amazing games with Qt 5, C++, and Qt Quick. ISBN 978-1-78839-999-9, Copyright © 2017 Packt Publishing)

p.s.

# Выдержка из книги:

## Предисловие

Как ведущий межплатформенный инструментарий для всех значительных настольных, мобильных, и встроенных платформ, пакет библиотек и инструментов Qt становится более популярным изо дня в день. Книга поможет изучить основные элементы пакета библиотек и инструментов Qt и снабдит необходимыми комплектами инструментов для построения приложений и игр. Книга разработана в виде руководства для начинающих, чтобы программистам, плохо знакомым с пакетом Qt, начать обучение с основ, таких как объекты(objects), базовые классы(core classes), виджеты(widgets) и новые функциональные возможности в пакете Qt версии 5.9, и закончить обучение на уровне компетенции, где они могут создать пользовательское приложение с применением наиболее успешной практики программирования с использованием пакета Qt.
Наше путешествие начнется с краткого введения в то, как создать приложение и подготовить рабочую среду построения и для настольных и для мобильных платформ. Затем мы погрузимся глубже в основы создания графических интерфейсов пользователя и в базовые понятия пакета библиотек и инструментов Qt по обработке данных и их отображению. По мере чтения глав, вы обучитесь обогащению своих игр, реализуя связь по сети(network connectivity) и используя написание скриптов(scripting). Вы погрузитесь в Qt Quick, OpenGL и различные инструменты для добавления логики игры, разработки анимации, добавления физики игры, обработки ввода игрового пульта и построения удивительных UI-интерфейсов пользователя для игр. К концу этой книги вы изучите использование функциональностей мобильных устройств, таких как датчики и службы геолокации, для построения привлекательных впечатлений пользователя.

## Для кого предназначена эта книга?

Эта книга будет интересна и полезна программистам и разработчикам приложений и UI-интерфейсов пользователя, у которых есть базовые знания о языке C++. Кроме того, некоторые части пакета Qt позволяют использовать язык JavaScript, и поэтому базовые знания этого языка также будут полезны. Предыдущий опыт работы с пакетом Qt не требуется. Разработчики максимум с годичным опытом работы с пакетом Qt также извлекут выгоду из тем, затронутых в этой книге.

## Что рассматривает эта книга?

**Глава 1 «Введение в пакет Qt»** ознакомляет со стандартным поведением, которое требуется при создании меж-платформенных приложений и показывает немного истории пакета Qt и как он развился в течение долгого времени с акцентом на новые архитектурные изменения в пакете Qt.

**Глава 2 «Установка»** ведет через процесс установки двоичного выпуска пакета Qt для настольных платформ, настраивая связанную IDE-среду разработки Qt Creator, и рассматривая различные параметры конфигурации, связанные с межплатформенным программированием.

**Глава 3 «Qt GUI-программирование»** показывает вам, как создать классические интерфейсы пользователя с использованием модуля виджетов Qt Widgets. Это также знакомит с процессом компиляции приложений с использованием пакета Qt.

**Глава 4 «Уникальная 2D-графика с графическим видом Graphics View»** знакомит с объектно-ориентированной 2D-графикой в пакете Qt. Вы изучите, как использовать встроенные элементы для составления финальных композиций, а также создать дополнительные собственные элементы.

**Глава 5 «Анимации в графическом виде Graphics View»** описывает фреймворк анимации Qt Animation, систему свойств(property system) и показывает, как реализовать анимации в графическом виде Graphics View. Глава проведет через процесс создания игры с 2D-графикой и анимациями.

**Глава 6 «Основы фреймворка Qt Core»** раскрывает понятия, связанные с обработкой данных и отображением в пакете Qt — обработкой данных файлов в различных форматах, обработка Unicode-текста и отображение видимых пользователем строк на различных языках и соответствия регулярных выражений.

**Глава 7 «Сети»** демонстрирует сетевые IP-технологии, доступные в пакете Qt. Она обучит вас тому, как соединиться с TCP-серверами, реализовать TCP-сервер и реализовать быструю коммуникацию через UDP-протокол.

**Глава 8 «Уникальные виджеты»** описывает целый механизм, связанный с программным 2D-рендерингом в пакете Qt, и научит созданию собственных классов виджетов с уникальной функциональностью.

**Глава 9 «Использование библиотек 3D-графики OpenGL и Vulkan в Qt-приложениях»** обсуждает возможности пакета Qt, связанные с ускоренным выводом 3D-графики. Вы изучите, как выполнить быстрое 3D-рисование с использованием API-интерфейсов приложения для разработки(application programming interfaces; APIs) для библиотек 3D-графики OpenGL и Vulkan и с использованием удобных Qt-оберток(Qt wrappers) для них.

**Глава 10 «Написание скриптов»** касается преимуществ написания скриптов для приложений. Она обучит вас тому, как использовать движок выполнения скриптов(scripting engine) для игры при помощи языков JavaScript или Python.

**Глава 11 «Введение в Qt Quick»** обучит вас тому, как программировать гибкие пользовательские интерфейсы, независимые от разрешения дисплея(resolution-independent), используя декларативный QML-движок времени выполнения и Qt Quick-среду окружения графа сцены.

**Глава 12 «Настройка в Qt Quick»** фокусируется на том, как реализовать новые графические элементы в Qt Quick-среде окружения и реализовать пользовательскую обработку событий.

**Глава 13 «Анимации в Qt Quick-играх»** знакомит со способами выполнить анимации в Qt Quick-среде окружения и дать больше подсказок для реализации игр в Qt Quick-среде окружения.

**Глава 14 «Продвинутые визуальные эффекты в Qt Quick»** рассматривает некоторые продвинутые понятия, позволяющие вам создавать действительно уникальные графические эффекты в Qt Quick-среде окружения.

**Глава 15 «3D-графика в Qt»** схематично описывает использование высокоуровневого API для 3D-графики из пакета Qt и показывает, как реализовать 3D-игру с анимацией.

**Глава 16 «Разное и продвинутые понятия»** демонстрирует важные аспекты программирования с использованием пакета Qt, которые не приводились в других главах, но которые могут быть важны для программирования игр. Эта глава доступна в онлайне по адресу https://www.packtpub.com/sites/default/files/downloads/MiscellaneousandAdvancedConcepts.pdf.

## Что потребуется для работы с книгой?

Вам не требуется иметь или установить какое-либо программное обеспечение прежде, чем начнете работать с книгой. Общих операционных систем Windows, Linux или MacOS должно быть достаточно. Глава 2 «Установка» содержит детализированные инструкции о загрузке и установке всего необходимого.

Книга:
https://www.packtpub.com/product/game-programming-using-qt-5-beginner-s-guide-second-edition/9781788399999

Загрузка кода примеров для этой книги:
https://github.com/PacktPublishing/Game-Programming-Using-Qt-5-Beginners-Guide-Second-Edition


Загрузка цветных изображений для этой книги:
Нет.
