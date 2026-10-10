---
title: "Glyph"
linktitle: "Glyph"
second_title: "Aspose.Words für Java"
description: "Stellt ein Glyph in Java dar."
type: docs
weight: 359
url: /de/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Stellt ein Glyph dar
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Gibt eine Kopie dieser Instanz zurück. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | Vorschubbreite, die die Platzierung des nachfolgenden Glyphs angibt. |
| [getAdvanceOffset()](#getAdvanceOffset) | Horizontaler (x)-Versatz relativ zur Glyph-Position. |
| [getAscenderOffset()](#getAscenderOffset) | Vertikaler (y)-Versatz relativ zur Glyph-Position. |
| [getGlyphIndex()](#getGlyphIndex) | Index des Glyphs (GID) in der physischen Schrift. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Gibt die Breite (Vorschub) des Glyphs in Punkten zurück. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| glyphIndex | int | Glyph-Index. |
| advance | short | Vorschub-Metrik des Glyphs. |
| advanceOffset | short | Horizontaler (x)-Versatz. |
| ascenderOffset | short | Vertikaler (y)-Versatz. |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Gibt eine Kopie dieser Instanz zurück.

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


Vorschubbreite, die die Platzierung des nachfolgenden Glyphs angibt.

**Returns:**
short - Der entsprechende short-Wert.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Horizontaler (x)-Versatz relativ zur Glyph-Position. Wird hauptsächlich verwendet, um Markierungen (wie Diakritika) an Grundzeichen anzuhängen.

**Returns:**
short - Der entsprechende short-Wert.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Vertikaler (y)-Versatz relativ zur Glyph-Position. Wird hauptsächlich verwendet, um Markierungen (wie Diakritika) an Grundzeichen anzuhängen.

**Returns:**
short - Der entsprechende short-Wert.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Index des Glyphs (GID) in der physischen Schrift.

**Returns:**
int - Der entsprechende int-Wert.
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Gibt die Breite (Vorschub) des Glyphs in Punkten zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
