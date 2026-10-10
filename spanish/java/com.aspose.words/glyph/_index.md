---
title: "Glyph"
linktitle: "Glyph"
second_title: "Aspose.Words para Java"
description: "Representa un glifo en Java."
type: docs
weight: 359
url: /es/java/com.aspose.words/glyph/
---

**Inheritance:**
java.lang.Object
```
public class Glyph
```

Representa un glifo
## Constructores

| Constructor | Descripción |
| --- | --- |
| [Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)](#Glyph-int-short-short-short) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [deepClone()](#deepClone) | Devuelve una copia de esta instancia. |
| [getAdditionalAdvance()](#getAdditionalAdvance) |  |
| [getAdvance()](#getAdvance) | Ancho de avance que indica la posición del glifo siguiente. |
| [getAdvanceOffset()](#getAdvanceOffset) | Desplazamiento horizontal (x) relativo a la posición del glifo. |
| [getAscenderOffset()](#getAscenderOffset) | Desplazamiento vertical (y) relativo a la posición del glifo. |
| [getGlyphIndex()](#getGlyphIndex) | Índice del glifo (GID) en la fuente física. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Devuelve el ancho (avance) del glifo en puntos. |
### Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset) {#Glyph-int-short-short-short}
```
public Glyph(int glyphIndex, short advance, short advanceOffset, short ascenderOffset)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| glyphIndex | int | Índice del glifo. |
| advance | short | Métrica avanzada del glifo. |
| advanceOffset | short | Desplazamiento horizontal (x). |
| ascenderOffset | short | Desplazamiento vertical (y). |

### deepClone() {#deepClone}
```
public Glyph deepClone()
```


Devuelve una copia de esta instancia.

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


Ancho de avance que indica la posición del glifo siguiente.

**Returns:**
short - El valor short correspondiente.
### getAdvanceOffset() {#getAdvanceOffset}
```
public short getAdvanceOffset()
```


Desplazamiento horizontal (x) relativo a la posición del glifo. Usado principalmente para adjuntar marcas (como diacríticos) a los caracteres base.

**Returns:**
short - El valor short correspondiente.
### getAscenderOffset() {#getAscenderOffset}
```
public short getAscenderOffset()
```


Desplazamiento vertical (y) relativo a la posición del glifo. Usado principalmente para adjuntar marcas (como diacríticos) a los caracteres base.

**Returns:**
short - El valor short correspondiente.
### getGlyphIndex() {#getGlyphIndex}
```
public int getGlyphIndex()
```


Índice del glifo (GID) en la fuente física.

**Returns:**
int - El valor  int  correspondiente.
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Devuelve el ancho (avance) del glifo en puntos.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
