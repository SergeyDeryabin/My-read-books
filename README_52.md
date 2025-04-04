### Пятьдесят(и более) штрихов о прочитанных(переведённых) книгах. 
### Переводы этих книг посвящены Дерябиной(Гуглиной) Ирине Ивановне (1950 - 2003 г.г.) 

### Штрих пятьдесят второй. 2024 год.


# Селим Арсевер. Эссенция разработки игр с использованием фреймворка jQuery. Изучите, как сделать забавные и захватывающие многоплатформенные игры, используя фреймворк jQuery. 

## (Selim Arsever. jQuery Game Development Essentials. Learn how to make fun and addictive multi-platform games using jQuery, ISBN 978-1-84969-506-0, Copyright © 2013 Packt Publishing) 

 
p.s.

# Выдержка из книги:


## Предисловие

Написание игр является не только забавой, но также и очень хорошим способом детального изучения новых технологий. Даже при том, что HTML и JavaScript были задуманы не для выполнения игр, но за последние несколько лет, произошло множество событий, сделавших написание игр на языке JavaScript жизнеспособным решением:
 Производительность JavaScript-движков у браузеров улучшилась существенно и  современные движки в десять раз быстрее современных движков 2008 года
 Фреймворк jQuery и другие подобные библиотеки сделали работу с DOM-моделью документа столь безболезненной, как это может быть 
 Фреймворк Flash потерял много должных позиций, частично, из-за отсутствия на устройствах с ОС iOS
 Консорциум W3C запустил работу над многими, ориентированными на игры, программными API-интерфейсами, такими как холст canvas, WebGL и полноэкранные программные API-интерфейсы
В этой книге вы сделаете три игры и изучите огромное количество техник и методов. Вы не только будете в состоянии делать и использовать свои собственные игры, но самое главное вы весело проведете время, делая так!



## Для кого предназначена эта книга?

Основной аудиторией для этой книги являются веб-разработчики-новички, с некоторым опытом в языке программирования JavaScript и в фреймворке(библиотеке) jQuery. Так как часть кода на стороне сервера реализована на языке программирования PHP, то если ли у вас есть некоторое знание его,  то это также поможет, но если вы более уверенно знаете другой серверный язык, то вы могли бы использовать его, вместо PHP, без слишком большой проблемы.

Чтобы наслаждаться этой книгой, вам вообще не требуются никакие предварительные знания разработки игр!

  
 
## Что рассматривает эта книга?

**Глава 1 «Фреймворк jQuery для игр»**  предоставляет всесторонний взгляд на функции фреймворка jQuery, которые могли бы быть полезны для разработки игр.

**Глава 2 «Создание нашей первой игры»** показывает процесс создания простой игры со спрайтами, анимацией и предварительной загрузкой.

**Глава 3 «Лучше, быстрее, но не тяжелее»**  оптимизирует игру, которую мы видели в главе 2 «Создание нашей первой игры», с помощью различных техник и методов, таких как встраивание тайм-аута, опрос клавиатуры  и HTML-фрагменты.

**Глава 4 «Поперечный взгляд»** кодирует игру фреймворка с картами в виде карты из тайлов(плиток) и обнаружением столкновений. 

**Глава 5 «Помещение предметов в перспективу»**   создает ортогональную RPG-игру с оптимизацией карты из тайлов(плиток), заграждением(окклюзией) спрайтов и лучшим обнаружением столкновений.

**Глава 6 «Добавление уровней к играм»**  расширяет игру из главы 4 «Поперечный взгляд», путем добавления множества уровней, с использованием технологий JSON и AJAX.

**Глава 7 «Создание многопользовательской игры»** преобразует игру из главы 5 «Помещение предметов в перспективу», чтобы поддерживать множество игроков на множестве машин.

**Глава 8 «Давайте станем социальными»**  интегрирует игру-платформер с соцсетями Facebook и Twitter, а также создает доску лидеров, защищенную от вмешательства.

**Глава 9 «Создание мобильной игры»** оптимизирует игру из главы 5 «Помещение предметов в перспективу», для мобильных устройств и управления касанием.

**Глава 10 «Создание некоторого шума»**   добавляет звуковые эффекты и музыку к игре, с помощью аудио-элемента, программного  Web Audio API-интерфейса веб-аудио или технологии Flash.
 
  

 
## Что потребуется для работы с книгой?

Одно из преимуществ работы с веб-технологиями состоит том, что для старта разработки вам не требуется ни какое сложное или дорогостоящее программное обеспечение. Для игр, строго на стороне клиента, вам потребуется только ваш любимый редактор кода(или даже простой текстовый редактор, если вы не возражаете против работы без какой-либо подсветки синтаксиса). Если вы еще не выбрали таковой, то есть много бесплатного программного обеспечения(ПО), которое можно попробовать, в пределах, начиная с ПО очень старой школы, таких как VIM (http://www.vim.org/) и Emacs(http://www.gnu.org/software/emacs/), продолжая ПО более современным, таким как Eclipse(http://www.eclipse.org/) и Aptana(http://www.aptana.com/), Notepad++(http://notepad-plus-plus.org/) или Komodo Edit (http://www.activestate.com/komodo-edit). Это только некоторые доступные редакторы, которые можно найти. Для языка программирования JavaScript вам не требуется многофункциональный редактор и поэтому просто используете более знакомый вам редактор.

Если вы хотите создать собственную графику, то вам также потребуется программное обеспечение редактирования изображений. Здесь снова, у вас есть большой выбор. Самое известное ПО с открытым исходным кодом Gimp(http://www.gimp.org/) и одно из моих любимых ПО, Pixen (http://pixenapp.com/).

Для части книги, которая нуждается в некоторых скриптах на стороне сервера, мы будем использовать языки PHP и MySQL. Если у вас нет в наличии   сервера, поддерживающего их, то чтобы установить их на вашей ПЭВМ, вы можете использовать продукты MAMP(http://www.mamp.info/), XAMPP(http://www.apachefriends.org/en/xampp.html), или EasyPHP(http://www.easyphp.org/), в зависимости от вашей ОС.


## Книга:
https://www.packtpub.com/en-us/product/jquery-game-development-essentials-9781849695060

## Загрузка кода примеров для этой книги:
https://github.com/onaluf/jQueryGameDevEssentials


## Загрузка цветных изображений для этой книги:
Нет. Но есть авторский обзор книги(англ.) со снимками экрана игр.
https://jquerygamedevelopment.com/
