---
title: "Glif"
linktitle: "Glif"
second_title: "Aspose.Words Java için"
description: "Java'da bir glifi temsil eder."
type: docs
weight: 359
url: /tr/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Bir glifi temsil eder
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | Bu örneğin bir klonunu döndürür. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | Sonraki glif için yerleşimi gösteren ilerleme genişliği. |
| [getAdvanceOffset()](#getAdvanceOffset) | Glif konumuna göre yatay (x) offset. |
| [getAscenderOffset()](#getAscenderOffset) | Glif konumuna göre dikey (y) offset. |
| [getGlyphIndex()](#getGlyphIndex) | Fiziksel fonttaki glifin (GID) indeksi. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Glifin nokta cinsinden genişliğini (ilerleme) döndürür. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| glyphIndex | int | Glif indeksi. |
| ilerleme | short | Glifin ilerleme ölçütü. |
| advanceOffset | short | Yatay (x) ofset. |
| ascenderOffset | short | Dikey (y) ofset. |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Bu örneğin bir klonunu döndürür.

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


Sonraki glif için yerleşimi gösteren ilerleme genişliği.

**Returns:**
short - İlgili  short  değer.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Glif konumuna göre yatay (x) ofset. Çoğunlukla işaretleri (örneğin diakritik işaretler) temel karakterlere eklemek için kullanılır.

**Returns:**
short - İlgili  short  değer.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Glif konumuna göre dikey (y) ofset. Çoğunlukla işaretleri (örneğin diakritik işaretler) temel karakterlere eklemek için kullanılır.

**Returns:**
short - İlgili  short  değer.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Fiziksel fonttaki glifin (GID) indeksi.

**Returns:**
int - İlgili  int  değeri.
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Glifin nokta cinsinden genişliğini (ilerleme) döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
