### Пятьдесят штрихов о прочитанных(переведённых) книгах. 
### Штрих тринадцатый. 2015 год.

# Ричард Эден. jMonkeyEngine 3.0. Книга рецептов. Более 80 практических рецептов для расширения и обогащения вашего уровня владения jMonkeyEngine с фокусом на разработке игр.
## (Rickard Edén. jMonkeyEngine 3.0 Cookbook. Over 80 practical recipes to expand and enrich your jMonkeyEngine skill set with a close focus on game development . ISBN 978-1-78328-647-8, Copyright © 2014 Packt Publishing)

p.s.

# Выдержка из книги:

## Предисловие

Полная цель этой книги состоит в том, чтобы предоставить вам обширный комплект практических советов по разработке для движка jMonkeyEngine, который поможет вам быть хорошо подготовленным к широкому диапазону проектов. 
Рецепты написаны с практической точки зрения, и я стремился удостовериться, что у каждого рецепта есть результат, который может использоваться напрямую в игре. Исключением из этого стиля является глава 7 "Организация сети на базе SpiderMonkey", где начнем с абсолютного нулевого уровня и будем работать сами вверх по уровням. Глава 1 "Хаб SDK разработки игр", также отличается по стилю изложения, поскольку она содержит несколько более общих советов, применимых к разработке в целом. 
Из-за разнообразия проектов игр, использовался другой принцип создания рецептов, которые предполагают широкую возможность использования. Некоторые более продвинутые рецепты являются исключениями из этого правила. Они имеют более узкое использование, но содержат технологические методы, которые могут быть применены к другим реализациям. Во многих рецептах будут рассмотрены игры FPS, RTS и RPG. Естественно, в пределах этих жанров, игры также широко отличаются друг от друга, но надеемся, что вы обнаружите, что примеры с минимальными модификациями могут быть использованы в вашем проекте игры. В целом я надеюсь, что эта книга предоставит вам много советов о преодолении общих барьеров в проектах игр для того, чтобы вы могли сосредоточиться на творческих частях игры, которые делают вашу игру уникальной. 

### Общие понятия разработки с движком jMonkeyEngine

Некоторые общие понятия разработки при использовании движка jMonkeyEngine:
* Spatial(Пространственный тип): Главным для всех предметов в графе сцены является понятие пространственный тип. В движке jMonkeyEngine это понятие реализовано в абстрактном классе, задающем перенос(translation; местоположение/location), поворот(вращение; rotation) и масштабирование(scale) объекта. Представляйте его как чисто логический объект без физического тела. Spatial-тип(Пространственный тип) расширяется или в тип Geometry (Геометрия) или в тип Node(Узел).
* Geometry(Геометрия): Он расширяет класс Spatial(Пространственный тип). Этот класс является тем, что дает пространственному объекту его физическое присутствие(внешний вид) в мире. Он содержит экземпляр класса Mesh(Мешь; набор мноугольников), задающий форму и фигуру и содержит экземпляр класса Material(Материал), говорящий нам о том, на что похожа поверхность меша.
* Node(Узел): Он расширяет класс Spatial(Пространственный). Он может содержать несколько присоединенных дочерних объектов, и может в свою очередь быть присоединенным к родительскому узлу. Так как он посути является классом Spatial(Пространственный), то у него есть перенос(translation), поворот(rotation) и масштабирование(scale), которые он передает по наследству присоединенным дочерним объектам. В отличие от класса Geometry(Геометрия), он не может содержать в себе экземпляры класса Mesh(мешь; набор мноугольников). Он сам по себе не имеет видимого присутствия в мире.
* Transforms(Преобразования): Перенос, поворот и масштабирование обычно относятся к Spatial-преобразованиям. Spatial-объекты имеют преобразования и в локальные координаты и в мировые координаты. Преобразование в локальные координаты всегда происходит относительно его родительского узла (если таковой имеется). Преобразованием в мировые координаты является абсолютное преобразование со всеми возможными родительскими преобразованиями, переданными по наследству, вместе. В качестве примера, вообразите перенос локальных координат вашей позиции на Земле. Вашим переносом мировых координат мог бы быть перенос локальных координат вашей позиции на Земле, добавленным к переносу локальных координат Земли в его орбите вокруг Солнца. Обычно, вы будете работать только с преобразованиями локальных координат. Преобразования мировых координат, обработаны движком.
* Mesh(Мешь): состоит из треугольников. В меше вы найдете длинные списки, именуемые буферами, детализирующими точки этих треугольников (вершины; vertices) и то как сделаны поверхности этих треугольников(индексы; indices), их цвета(colors), нормали(normals) и другие данные. Обычно, вы загружаете 3D-модель с диска, без необходимости заботы о ее внешнем виде на этом уровне, но в некоторых рецептах меши будут созданы с нуля, и я вам рекомендую иметь базовое понимание мешей при разработке 3D-игр.
* Material(Материал): определяет поверхность меша. Он с тыльной стороны поддержан типом определения материала(MatDef), обычно содержащий вершинный шейдер(a vertex shader) и фрагментный шейдер(a fragment shader). Сложность простирается от простого выбора цвета или текстуры для меша, до настроек, которые изменяют форму меша. Вы получите многое при помощи предопределенного определения материала MatDef в движке jMonkeyEngine. 
Некоторые базовые понятия движка, относящиеся к типу "должен - знать"(must-know). Следующие понятия можно считать относящимися к подтипу "хорошо, что их знаешь"(nice-to-know). На своем опыте я знаю, что они -являются теми понятиями, о которых жаль, что не знали их прежде до того, как приложения были разработаны. Они будут также использоваться вполне часто всюду в главах этой книги:
* AppState(Состояние приложения): объект, который затрагивает поведение целого приложения, и вы можете, например, использовать его для задания логики для различных частей приложения. Примером использования понятия могла быть ситуация, если у вас есть игра, которая заканчивается вариантами и на карте похода, и на земле, то в разных вариантов и ввод данных игроком, и логика игры, вероятно, отличались бы довольно сильно. При помощи класса AppState вы можете управлять кодом более легко и избежать классов-монстров.
* Control (тип контроллер): как и в случае с понятием AppState, это понятие является хорошим способом управления вашим кодом. Тип управления Control затрагивает пространственный тип Spatial, к которому он присоединен и обычно используется, чтобы придать пространственному типу Spatial специальные функциональности. Во многих главах вы увидите несколько примеров поведения типа контроллера Control, поэтому если вы предпочтете обучаться на практике, то вы найдете все для удовольствия.

## Для кого предназначена эта книга?

Эта книга идеально подходит пользователям промежуточного и продвинутого уровня владения движком для разработки игр jMonkeyEngine 3.0.
 

## Что рассматривает эта книга?

**Глава 1 «SDK Game Development Hub»** проведет тур вокруг SDK, не забывая об игре. Узнаете о встроенных функциях и подключаемых модулях(плагинах), облегчающих вашу жизнь.

**Глава 2 «Камеры и управление игрой»** содержит много конкретных способов использования камеры и управления аватаром для множества типов игр.
 
**Глава 3 «Построение мира»** исследует различные методы, которые вы можете использовать для создания и изменения окружения игр.

**Глава 4 «Освоение анимаций персонажей»** предоставляет вам материал изучению всего, что вы должны знать об управлении анимациями персонажей.

**Глава 5 «Искусственный интеллект»** содержит взгляд на основы и общие проблемы AI (Artificial Intelligence; Искусственный интелект) для игр.

**Глава 6 «GUI на базе изящного Nifty GUI-интерфейса»** содержит технологические методы по разработке набора стандартных пользовательских интерфейсов, необходимых для игр. 

**Глава 7 «Организация сети на базе SpiderMonkey»** является введением в сетевые протоколы UDP/TCP, используемые в играх на базе jMonkeyEngine. 

**Глава 8 «Физика на базе библиотеки Bullet»** обучит вас реализации библиотеки Bullet и ее применению в ваших играх. 
 
**Глава 9 «Подъем нашей игры на следующий уровень»** расскажет вам, что сделать, когда ваши игровая механика и игра достигли зрелости. Однако, вы почувствуете, что игре чего- то не хватает. Эта глава покажет различные методы для продвижения вашей игры на новый уровень в части  качества.

**Приложение «Дополнительная информация»** содержит некоторые универсальные фрагменты кода и инструкции о том, как они могут использоваться в главах книги. Здесь также есть некоторые полные сегменты кода для рецептов, которые являются слишком длинными, чтобы включать их в сами главы.

## Книга:
https://www.packtpub.com/product/jmonkeyengine-3-0-cookbook/9781783286478

## Загрузка кода примеров для этой книги:
Нет.

## Загрузка цветных изображений для этой книги:
https://static.packt-cdn.com/downloads/6478OS_ColoredImages.pdf
