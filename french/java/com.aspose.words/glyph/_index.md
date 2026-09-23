---
title: "Glyph"
linktitle: "Glyph"
second_title: "Aspose.Words pour Java"
description: "Représente un glyph en Java."
type: docs
weight: 359
url: /fr/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Représente un glyphe
## Constructors

| Constructor | Description |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [deepClone()](#deepClone) | Renvoie un clone de cette instance. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | Largeur d'avance indiquant le placement du glyph suivant. |
| [getAdvanceOffset()](#getAdvanceOffset) | Décalage horizontal (x) relatif à la position du glyph. |
| [getAscenderOffset()](#getAscenderOffset) | Décalage vertical (y) relatif à la position du glyph. |
| [getGlyphIndex()](#getGlyphIndex) | Index du glyph (GID) dans la police physique. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Renvoie la largeur (avance) du glyph en points. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| glyphIndex | int | Index du glyph. |
| advance | short | Métrique avancée du glyphe. |
| advanceOffset | short | Décalage horizontal (x). |
| ascenderOffset | short | Décalage vertical (y). |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Renvoie un clone de cette instance.

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


Largeur d'avance indiquant le placement du glyph suivant.

**Returns:**
short - La valeur short correspondante.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Décalage horizontal (x) relatif à la position du glyphe. Principalement utilisé pour attacher des marques (comme les diacritiques) aux caractères de base.

**Returns:**
short - La valeur short correspondante.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Décalage vertical (y) relatif à la position du glyphe. Principalement utilisé pour attacher des marques (comme les diacritiques) aux caractères de base.

**Returns:**
short - La valeur short correspondante.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Index du glyph (GID) dans la police physique.

**Returns:**
int - La valeur int correspondante.
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Renvoie la largeur (avance) du glyph en points.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
