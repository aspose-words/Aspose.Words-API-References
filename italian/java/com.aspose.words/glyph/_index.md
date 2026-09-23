---
title: "Glyph"
linktitle: "Glyph"
second_title: "Aspose.Words per Java"
description: "Rappresenta un glifo in Java."
type: docs
weight: 359
url: /it/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Rappresenta un glifo
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [deepClone()](#deepClone) | Restituisce una copia di questa istanza. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | Larghezza di avanzamento che indica la posizione per il glifo successivo. |
| [getAdvanceOffset()](#getAdvanceOffset) | Offset orizzontale (x) relativo alla posizione del glifo. |
| [getAscenderOffset()](#getAscenderOffset) | Offset verticale (y) relativo alla posizione del glifo. |
| [getGlyphIndex()](#getGlyphIndex) | Indice del glifo (GID) nel font fisico. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Restituisce la larghezza (avanzamento) del glifo in punti. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| glyphIndex | int | Indice del glifo. |
| avanzamento | short | Metrica avanzata del glifo. |
| advanceOffset | short | Scostamento orizzontale (x). |
| ascenderOffset | short | Scostamento verticale (y). |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Restituisce una copia di questa istanza.

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


Larghezza di avanzamento che indica la posizione per il glifo successivo.

**Returns:**
short - Il valore short corrispondente.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Scostamento orizzontale (x) relativo alla posizione del glifo. Usato principalmente per collegare segni (come i diacritici) ai caratteri base.

**Returns:**
short - Il valore short corrispondente.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Scostamento verticale (y) relativo alla posizione del glifo. Usato principalmente per collegare segni (like diacritics) ai caratteri base.

**Returns:**
short - Il valore short corrispondente.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Indice del glifo (GID) nel font fisico.

**Returns:**
int - Il valore  int  corrispondente.
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Restituisce la larghezza (avanzamento) del glifo in punti.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
