---
title: "Glyph"
linktitle: "Glyph"
second_title: "Aspose.Words لـ Java"
description: "يمثل glyph في Java."
type: docs
weight: 359
url: /ar/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

يمثل رمزًا
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | يُهيئ نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | يرجع نسخة مستنسخة من هذه النسخة. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | العرض المتقدم الذي يحدد موضع glyph التالي. |
| [getAdvanceOffset()](#getAdvanceOffset) | الإزاحة الأفقية (x) بالنسبة إلى موضع glyph. |
| [getAscenderOffset()](#getAscenderOffset) | الإزاحة العمودية (y) بالنسبة إلى موضع glyph. |
| [getGlyphIndex()](#getGlyphIndex) | فهرس glyph (GID) في الخط الفعلي. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | يرجع عرض (متقدم) glyph بالنقاط. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


يُهيئ نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| glyphIndex | int | فهرس Glyph. |
| advance | short | مقياس التقدم للـ glyph. |
| advanceOffset | short | الإزاحة الأفقية (x). |
| ascenderOffset | short | الإزاحة العمودية (y). |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


يرجع نسخة مستنسخة من هذه النسخة.

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


العرض المتقدم الذي يحدد موضع glyph التالي.

**Returns:**
short - القيمة المقابلة  short  .
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


الإزاحة الأفقية (x) نسبةً إلى موضع glyph. تُستخدم غالبًا لإرفاق العلامات (مثل الحركات) إلى الأحرف الأساسية.

**Returns:**
short - القيمة المقابلة  short  .
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


الإزاحة العمودية (y) نسبةً إلى موضع glyph. تُستخدم غالبًا لإرفاق العلامات (مثل الحركات) إلى الأحرف الأساسية.

**Returns:**
short - القيمة المقابلة  short  .
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


فهرس glyph (GID) في الخط الفعلي.

**Returns:**
int - القيمة المقابلة  int .
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


يرجع عرض (متقدم) glyph بالنقاط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
