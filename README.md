# Урок 4: Освоение Блочной Модели и Макетирования в CSS
Макетирования в CSS" - это тема, которая позволит студентам глубже понять, как устроены веб-страницы и как их структурировать эффективно и красиво. В этом уроке вы сможете рассмотреть ключевые аспекты блочной модели CSS, такие как внешние и внутренние отступы, границы, размеры элементов, а также основы создания макетов с использованием CSS, включая флексбокс и грид. Это знание является фундаментальным для любого веб-разработчика.

#### Понятие блочной модели.:
Свойства margin, border, padding. </br>

Применить к каждому элементу различные значения margin, border, и padding, наблюдая за изменениями в расположении и размерах блоков. </br>
#### Основы Flexbox: display: flex;:
🔗[Пример работы flex](https://html5.by/blogdemo/flexbox/flex-direction-align-justify.html).</br>
display: flex; — это CSS свойство, которое активирует гибкую ("flexible") модель макета для контейнера элементов. Это означает, что все дочерние элементы данного контейнера становятся flex-элементами и подчиняются особым правилам расположения и выравнивания, определенным в этой модели.

Вот ключевые особенности и преимущества использования display: flex;

Гибкое выравнивание элементов: Flexbox позволяет легко выравнивать элементы горизонтально и вертикально внутри контейнера, используя свойства, такие как justify-content и align-items.

Изменение размеров элементов: Flexbox позволяет автоматически изменять размеры flex-элементов для заполнения доступного пространства в контейнере или для сжатия их, если пространства недостаточно, используя свойства flex-grow, flex-shrink и flex-basis.

Одномерное макетирование: Flexbox идеально подходит для создания одномерных макетов, то есть макетов, где важно управление пространством в одном направлении (либо по горизонтали, либо по вертикали).

Отзывчивый дизайн: Flexbox облегчает создание макетов, которые адаптируются к разным размерам экрана, что делает его мощным инструментом для разработки адаптивных веб-страниц.
</br>Основные свойства: `Flexbox`: </br> `flex-direction`,</br> `justify-content`,</br> `align-items`,</br> `flex-wrap`. </br>
Создание гибких макетов с помощью Flexbox. </br>

#### justify-content – выравнивание по главной оси.
CSS свойство justify-content определяет то, как будут выровнены элементы вдоль главной оси.

Доступные значения `justify-content`:
* `flex-start` (значение по умолчанию) : блоки прижаты к началу главной оси
* `flex-end`: блоки прижаты к концу главной оси
* `center`: блоки располагаются в центре главной оси
* `space-between`: первый блок располагается в начале главной оси, последний блок – в конце, все остальные блоки равномерно распределены в оставшемся пространстве.
* `space-around`: все блоки равномерно распределены вдоль главной оси, разделяя все свободное пространство поровну.

#### align-items – выравнивание по поперечной оси.
Css свойство align-items определяет то, как будут выровнены элементы вдоль поперечной оси.
Доступные значения align-items:

* flex-start: блоки прижаты к началу поперечной оси
* flex-end: блоки прижаты к концу поперечной оси
* center: блоки располагаются в центре поперечной оси
* baseline: блоки выровнены по их baseline
* stretch (значение по умолчанию) : блоки растянуты, занимая все доступное место по поперечной оси, при этом все же учитываются min-width/max-width, если таковые заданы.
* В CSS, родительские и дочерние элементы являются частью иерархии документа HTML. Понимание этой иерархии важно для эффективного применения стилей к элементам веб-страницы.

### Родительские Элементы (Parent Elements)

* Родительский элемент - это элемент, который содержит в себе другие элементы.
* Например, в HTML-структуре <div> может быть родительским элементом для `<p>`, если <p> находится внутри `<div>`.
Дочерние Элементы (Child Elements)
Дочерние элементы - это элементы, которые находятся внутри другого элемента.
В предыдущем примере `<p>` является дочерним элементом для `<div>`.
Примеры CSS Селекторов
Прямой потомок (Child Selector):
* `div > p` - выберет все `<p>`, которые являются непосредственными потомками <div>.
Все потомки (Descendant Selector):
* `div p` - выберет все `<p>`, которые находятся внутри `<div>`, включая те, которые глубже по иерархии.
Смежные братья и сестры (Adjacent Sibling Selector):
* `h1 + p` - выберет `<p>`, который непосредственно следует за h1.
Общие братья и сестры (General Sibling Selector):
* `h1 ~ p` - выберет все `<p>`, которые следуют за h1 на том же уровне иерархии.
  
Применение Стилей

Применяя стили к родительскому элементу, вы можете влиять на стилизацию всех дочерних элементов. Например, если вы задаете шрифт для div, этот шрифт будет применен ко всем текстовым элементам внутри этого div, если только для них не заданы индивидуальные стили.</br>

Также, вы можете применять стили специфически к дочерним элементам, используя соответствующие селекторы.</br>
Каскадирование и Наследование</br>

В CSS, стили "каскадируют" от родительских элементов к дочерним. Это означает, что если определенный стиль задан для родительского элемента, он будет применяться ко всем дочерним элементам, если только они не переопределены.</br>

Некоторые CSS-свойства наследуются от родительских элементов (например, font-family, color), а некоторые - нет (например, margin, border).</br>
Понимание этой иерархии и различных способов выбора элементов в CSS помогает создавать более точные и эффективные стили для веб-страниц.</br>
## Поля и отступы CSS: отличия свойств margin и padding
Создавать промежутки между элементами можно и тем, и другим способом, но если padding – это отступ от содержимого до края блока, то margin – это расстояние от одного блока до другого, межблоковое пространство. На скриншоте показан наглядный пример: </br>
Padding отделяет содержимое от границы блока т.е толкает контент внутрь родительского блого, а margin создает промежутки между блоками
Как видите, поля и отступы CSS отличаются между собой, хоть иногда без просмотра кода и нельзя определить, с помощью какого свойства задано расстояние. Это случается в тех случаях, когда отсутствует рамка или фон блока с содержимым.

Для установки полей или отступов в CSS от каждой стороны элемента существуют следующие свойства:</br>
Отступы:

* padding-top: значение;
* padding-right: значение;
* padding-bottom: значение;
* padding-left: значение;
Поля:

* margin-top: значение;
* margin-right: значение;
* margin-bottom: значение;
* margin-left: значение;
 

Значения могут быть указаны в любых единицах CSS – px, em, % и т. д. Пример: margin-top: 15px.

Также существует очень удобная вещь как сокращенная запись margin и padding CSS. Если вам необходимо задать поля или отступы для всех четырех сторон элемента, совсем необязательно записывать свойство для каждой стороны по отдельности. Всё делается проще: для margin и padding можно указывать сразу 1, 2, 3 или 4 значения. От количества значений зависит, как распределяются настройки:

* 4 значения: задаются отступы для всех сторон элемента в такой последовательности: сверху, справа, снизу, слева:
padding: 2px 4px 5px 10px;
* 3 значения: задается отступ сначала для верхней стороны, потом одновременно для левой и правой, а затем – для нижней:
padding: 3px 6px 9px;
* 2 значения: задаются отступы сначала одновременно от верхней и нижней стороны, а затем – одновременно для левой и правой:
padding: 6px 12px;
* 1 значение: задаются одинаковые отступы для всех сторон элемента:
padding: 3px;
Те же правила касаются и свойства margin CSS. Обратите внимание на то, что для margin можно использовать и отрицательные значения (например, -3px), которые иногда бывают весьма полезными


## ⛔️Теорию можно читать бесконечно ее в интернете море, быстрее перейдем к практике 
## 🏆 Задание 1:
🔗[Пройдите Задание Flexbox Froggy](https://flexboxfroggy.com/#ru).

## 🏆 Задание 2:
🔗[Ссылка на задание 2](https://greatcode.ru/lesson_4.2.html).

## 🏆 Задание 3:
🔗[Ссылка на задание 3](https://greatcode.ru/portfolio.html).

