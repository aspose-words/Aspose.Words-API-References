---
title: "Глиф"
linktitle: "Глиф"
second_title: "Aspose.Words для Java"
description: "Представляет глиф в Java."
type: docs
weight: 359
url: /ru/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Представляет глиф
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Возвращает клон этого экземпляра. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | Ширина продвижения, указывающая позицию для последующего глифа. |
| [getAdvanceOffset()](#getAdvanceOffset) | Горизонтальное (x) смещение относительно позиции глифа. |
| [getAscenderOffset()](#getAscenderOffset) | Вертикальное (y) смещение относительно позиции глифа. |
| [getGlyphIndex()](#getGlyphIndex) | Индекс глифа (GID) в физическом шрифте. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Возвращает ширину (продвижение) глифа в пунктах. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| glyphIndex | int | Индекс глифа. |
| advance | short | Продвинутая метрика глифа. |
| advanceOffset | short | Горизонтальное (x) смещение. |
| ascenderOffset | short | Вертикальное (y) смещение. |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Возвращает клон этого экземпляра.

**Returns:**
[Glyph](../../com.aspose.words/glyph/)
### getAdditionalAdvance() {#getAdditionalAdvance}
```
public short getAdditionalAdvance()
```




**Returns:**
short
### getAdvance() {#getAdvance}
```
public short getAdvance()
```


Ширина продвижения, указывающая позицию для последующего глифа.

**Returns:**
short - Соответствующее значение short.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Горизонтальное (x) смещение относительно позиции глифа. В основном используется для присоединения знаков (например, диакритических знаков) к базовым символам.

**Returns:**
short - Соответствующее значение short.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Вертикальное (y) смещение относительно позиции глифа. В основном используется для присоединения знаков (например, диакритических знаков) к базовым символам.

**Returns:**
short - Соответствующее значение short.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Индекс глифа (GID) в физическом шрифте.

**Returns:**
int — соответствующее значение  int .
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Возвращает ширину (продвижение) глифа в пунктах.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
