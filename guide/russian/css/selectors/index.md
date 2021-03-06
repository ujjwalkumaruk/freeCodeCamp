---
title: Selectors
localeTitle: Селекторы
---
# Селекторы

Селекторы - это правила CSS для таргетинга на HTML-элементы для применения стилей. Имена тегов, имена классов, идентификаторы и атрибуты - это некоторые из перехватчиков, используемых в качестве селекторов.

## Синтаксис селектора

Селекторы, расположенные в определенной последовательности, будут создавать правило для целевых элементов. Пример,

```css
/* selects anchor tags */ 
 a { 
    color: orange; 
 } 
 
 /* selects elements with hero class */ 
 .hero { 
    text-align: center; 
 } 
```

## Тип переключателей

Тип | Описание ------- | ------------ Селекторы типов | Имена тегов используются для выбора таких элементов, как `h1` или `a` . Универсальный селектор | Селектор, который применяется ко всем элементам. `div *` соответствует всем элементам в элементах div. Селектор атрибутов | Селекторы, которые нацеливают элементы на основе их атрибутов \[и, необязательно, их значений\]. `h1[title]` выбирает элементы `h1` с атрибутом `title` . Селектор классов | Селектор, который предназначен для элементов, используя их имена классов. ID Selector | Селектор, который использует идентификатор для целевых элементов. `#logo` выбирает элемент с `logo` качестве идентификатора. Селектор псевдокласса | Специальные селекторы, которые нацелены на элементы, основанные на их состоянии. `a:hover` селектор `a:hover` применяет стиль, когда указатель наводится на ссылки.

## Комбинаторы селектора

Комбинатор | Цель ----------- | ------------ `white space` | Комбинатор потомков. `.nav li` выбирает все `li` - `.nav` в классе `.nav` , включая вложенные элементы `li` . `>` | Детский комбинатор. `.menu > li` выбирает все li, которые являются прямыми `.menu` элементами элементов с классом `.menu` . `+` | Смежный комбинатор. `.logo + h1` целей `h1` , что является непосредственным родственным к `.logo` класса. `~` | Общий сборщик. `header ~ div` target `div` элементы, которые являются братьями и сестрами для элементов `header` .

В этом разделе описываются все эти избиратели.

#### Дополнительная информация:

Вы можете узнать больше о селекторах на этих ресурсах:

*   [Официальная спецификация CSS3](https://www.w3.org/TR/css3-selectors)
*   [Селекторная страница в Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Selectors)
*   [CSS-селектор Cheat Sheet на FreeCodeCamp](https://guide.freecodecamp.org/css/tutorials/css-selectors-cheat-sheet)

Селекторы в CSS (каскадные таблицы стилей) определяются на основе _специфики_ , с этим мы можем быть более конкретными в наших правилах стиля и переопределять другие правила, которые могут быть нацелены на один и тот же элемент, но не являются конкретными. Способ работы этой иерархии конкретных оснований зависит от веса, то есть элемент Селектор имеет вес 1 (один), селектор класса имеет вес 10 (десять), а селектор id имеет вес Сто (100). Мы можем комбинировать разные селекторы вместе, более конкретно, от элемента, который мы хотим изменить.

В качестве примера:

`css p { color: blue; } p .red { color: red; }` Наш селектор типов p выберет все элементы p в нашем html-документе, но он будет иметь только один вес. напротив, селектор классов имеет вес 11 по той причине, что мы объединяем селектор типов с селектором классов (этот селектор сопоставляет все элементы p с классом красного). - \* Прямо целевые правила всегда будут иметь приоритет над правилами, которые наследуют элементы от своего предка. - \* Спецификация применяется только тогда, когда несколько объявлений нацелены на один и тот же элемент, только тогда это правило применяется.  
\- \* Спецификация, как правило, почему некоторые из правил стиля не применяются к элементам, если вы ожидаете их.