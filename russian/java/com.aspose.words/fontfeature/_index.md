---
title: "FontFeature"
linktitle: "FontFeature"
second_title: "Aspose.Words для Java"
description: "Функции предоставляют информацию о том, как глифы используются в шрифте для рендеринга скрипта в Java."
type: docs
weight: 325
url: /ru/java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

Функции предоставляют информацию о том, как глифы используются в шрифте для рендеринга скрипта. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## Поля

| Поле | Описание |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | Чтобы минимизировать количество альтернативных глифов, иногда желательно разбить основной глиф символа на два или более глифа. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | Некоторые лигатуры были широко использованы в прошлом, но сегодня выглядят анахронично. |
| [KERNING](#KERNING) | Регулирует количество пространства между глифами, обычно для обеспечения оптически согласованного интервала между глифами. |
| [LINING_FIGURES](#LINING-FIGURES) | Эта функция меняет выбранные нелинейные цифры на линейные цифры. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | Эта функция меняет выбранные цифры из стандартного или линейного стиля в старый стиль. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | Заменяет глифы цифр, установленные с одинаковой (табличной) шириной, соответствующими глифами с шириной, зависящей от глифа (пропорциональной). |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | Stylistic Set 1 В дополнение к, или вместо, стилистических альтернатив отдельных глифов (см. функцию 'salt'), некоторые шрифты могут содержать наборы стилистических вариантов глифов, соответствующих частям набора символов, например. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | Stylistic Set 2 Эквивалентный тег OpenType: 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | Stylistic Set 3 Эквивалентный тег OpenType: 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | Stylistic Set 4 Эквивалентный тег OpenType: 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | Stylistic Set 5 Эквивалентный тег OpenType: 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | Stylistic Set 6 Эквивалентный тег OpenType: 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | Stylistic Set 7 Эквивалентный тег OpenType: 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | Stylistic Set 8 Эквивалентный тег OpenType: 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | Stylistic Set 9 Эквивалентный тег OpenType: 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | Stylistic Set 10 Эквивалентный тег OpenType: 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | Stylistic Set 11 Эквивалентный тег OpenType: 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | Stylistic Set 12 Эквивалентный тег OpenType: 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | Stylistic Set 13 Эквивалентный тег OpenType: 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | Stylistic Set 14 Эквивалентный тег OpenType: 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | Stylistic Set 15 Эквивалентный тег OpenType: 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | Stylistic Set 16 Эквивалентный тег OpenType: 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | Stylistic Set 17 Эквивалентный тег OpenType: 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | Stylistic Set 18 Эквивалентный тег OpenType: 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | Stylistic Set 19 Эквивалентный тег OpenType: 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | Стилистический набор 20 Эквивалентный тег OpenType: 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | Заменяет глифы цифр, заданные пропорциональной шириной, соответствующими глифами, заданными одинаковой (табличной) шириной. |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | Преобразует стандартные глифы в глифы, подходящие для прямого отображения в режиме вертикального письма. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | Заменяет некоторые глифы фиксированной ширины (половинной, третичной или четвертной) или пропорциональной ширины (в основном латинские или катакана) на формы, подходящие для вертикального письма (то есть повернутые на 90 градусов по часовой стрелке). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. В отличие от других функций лигатур, 'clig' указывает контекст, в котором лигатура рекомендуется. Эта возможность важна в некоторых дизайнах шрифтов и для декоративных лигатур. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig Эквивалентный тег OpenType: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. Эта функция охватывает те лигатуры, которые могут использоваться для особого эффекта по предпочтению пользователя. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig Эквивалентный тег OpenType: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


Чтобы минимизировать количество альтернативных глифов, иногда желательно разложить стандартный глиф символа на два или более глифа. Кроме того, может быть предпочтительно объединять стандартные глифы двух и более символов в один глиф для более эффективной обработки. Эта функция позволяет выполнять такую композицию/декомпозицию. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#ccmp Эквивалентный тег OpenType: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


Некоторые лигатуры были широко использованы в прошлом, но сегодня выглядят анахронично. Некоторые шрифты включают исторические формы как альтернативы, чтобы их можно было использовать для эффекта «период». Эта функция заменяет стандартные (текущие) формы на исторические альтернативы. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_fj\#hlig Эквивалентный тег OpenType: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


Регулирует расстояние между глифами, обычно для обеспечения оптически согласованного интервала между глифами. Хотя хорошо спроектированный шрифт имеет в целом постоянный интервал между глифами, некоторые комбинации глифов требуют корректировки для улучшения читаемости. Помимо стандартной коррекции в горизонтальном направлении, эта функция может предоставлять данные кернинга, зависящие от размера, через таблицы устройств, «сквозной» кернинг в направлении Y текста и корректировку размещения глифов независимо от корректировки шага. Обратите внимание, что эта функция может применяться к последовательностям из более чем двух глифов и не используется в моноширинных шрифтах. Также обратите внимание, что эта функция не применяется к тексту, установленному вертикально. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#kern Эквивалентный тег OpenType: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


Эта функция меняет выбранные нелинейные цифры на линейные цифры. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#lnum Эквивалентный тег OpenType: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


Эта функция меняет выбранные цифры из стандартного или линейного стиля в старый стиль. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#onum Эквивалентный тег OpenType: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


Заменяет глифы цифр, заданные одинаковой (табличной) шириной, соответствующими глифами, заданными индивидуальной (пропорциональной) шириной. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-pnum Эквивалентный тег OpenType: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


Заменяет последовательность глифов одним глифом, предпочтительным для типографических целей. Эта функция охватывает те лигатуры, которые сценарий определяет как обязательные для использования в обычных условиях. Эта функция важна для некоторых сценариев, чтобы обеспечить правильное формирование глифов. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#rlig Эквивалентный тег OpenType: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


Заменяет последовательность глифов одним глифом, который предпочтителен для типографических целей. Эта функция охватывает лигатуры, которые дизайнер/производитель считает нужным использовать в обычных условиях. Эквивалентный тег OpenType: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


Набор стилистических вариантов 1 В дополнение к, или вместо, стилистических альтернатив отдельных глифов (см. функцию 'salt'), некоторые шрифты могут содержать наборы стилистических вариантов глифов, соответствующие частям набора символов, например несколько вариантов строчных букв в латинском шрифте. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-ss01---ss20 Эквивалентный тег OpenType: 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


Stylistic Set 2 Эквивалентный тег OpenType: 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


Stylistic Set 3 Эквивалентный тег OpenType: 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


Stylistic Set 4 Эквивалентный тег OpenType: 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


Stylistic Set 5 Эквивалентный тег OpenType: 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


Stylistic Set 6 Эквивалентный тег OpenType: 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


Stylistic Set 7 Эквивалентный тег OpenType: 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


Stylistic Set 8 Эквивалентный тег OpenType: 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


Stylistic Set 9 Эквивалентный тег OpenType: 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


Stylistic Set 10 Эквивалентный тег OpenType: 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


Stylistic Set 11 Эквивалентный тег OpenType: 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


Stylistic Set 12 Эквивалентный тег OpenType: 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


Stylistic Set 13 Эквивалентный тег OpenType: 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


Stylistic Set 14 Эквивалентный тег OpenType: 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


Stylistic Set 15 Эквивалентный тег OpenType: 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


Stylistic Set 16 Эквивалентный тег OpenType: 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


Stylistic Set 17 Эквивалентный тег OpenType: 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


Stylistic Set 18 Эквивалентный тег OpenType: 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


Stylistic Set 19 Эквивалентный тег OpenType: 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


Стилистический набор 20 Эквивалентный тег OpenType: 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


Заменяет глифы цифр, заданные пропорциональными ширинами, соответствующими глифами с одинаковой (табличной) шириной. Табличные ширины обычно являются значением по умолчанию, но это нельзя считать безопасным предположением. Конечно, эта функция не будет присутствовать в моноширинных дизайнах. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-tnum Эквивалентный тег OpenType: 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


Преобразует глифы по умолчанию в глифы, подходящие для вертикального написания в прямом положении. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vert Эквивалентный тег OpenType: 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


Заменяет некоторые глифы фиксированной ширины (половинной, третьей или четверти) или пропорциональной ширины (в основном латинские или катакана) на формы, подходящие для вертикального написания (то есть повернутые на 90 градусов по часовой стрелке). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vrt2 Эквивалентный тег OpenType: 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontFeature) {#toString-int}
```
public static String toString(int fontFeature)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
