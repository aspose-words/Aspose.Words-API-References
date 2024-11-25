---
title: Glyph
linktitle: Glyph
second_title: Aspose.Words for Java
description: Represents a glyph in Java.
type: docs
weight: 347
url: /java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Represents a glyph
## Constructors

| Constructor | Description |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Initializes new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [deepClone()](#deepClone) | Returns a clone of this instance. |
| [getAdvance()](#getAdvance) | Advance width indicating placement for the subsequent glyph. |
| [getAdvanceOffset()](#getAdvanceOffset) | Horizontal (x) offset relative to glyph position. |
| [getAscenderOffset()](#getAscenderOffset) | Vertical (y) offset relative to glyph position. |
| [getGlyphIndex()](#getGlyphIndex) | Index of the glyph (GID) in the physical font. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Returns width (advance) of the glyph in points. |
| [setAdvance(short value)](#setAdvance-short) | Advance width indicating placement for the subsequent glyph. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Initializes new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| glyphIndex | int | Glyph index. |
| advance | short | Advance metric of the glyph. |
| advanceOffset | short | Horizontal (x) offset. |
| ascenderOffset | short | Vertical (y) offset. |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Returns a clone of this instance.

**Returns:**
[Glyph](../../com.aspose.words/glyph/)
### getAdvance() {#getAdvance}
```
public short getAdvance()
```


Advance width indicating placement for the subsequent glyph.

**Returns:**
short - The corresponding  short  value.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Horizontal (x) offset relative to glyph position. Mostly used to attach marks (like diacritics) to base characters.

**Returns:**
short - The corresponding  short  value.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Vertical (y) offset relative to glyph position. Mostly used to attach marks (like diacritics) to base characters.

**Returns:**
short - The corresponding  short  value.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Index of the glyph (GID) in the physical font.

**Returns:**
int - The corresponding  int  value.
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Returns width (advance) of the glyph in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
### setAdvance(short value) {#setAdvance-short}
```
public void setAdvance(short value)
```


Advance width indicating placement for the subsequent glyph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | short | The corresponding  short  value. |

