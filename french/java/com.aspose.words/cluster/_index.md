---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words pour Java"
description: "Encapsule les points de code et les glyphes composant un grapheme en Java."
type: docs
weight: 104
url: /fr/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Encapsule les points de code et les glyphes composant un graphème.
## Constructors

| Constructor | Description |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [deepClone()](#deepClone) | Renvoie un clone profond de cette instance. |
| [getCodepoints()](#getCodepoints) | Obtient les points de code du cluster. |
| [getCodepointsLength()](#getCodepointsLength) | Obtient le nombre total de points de code dans le [Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | Obtient les glyphes du cluster. |
| [getString()](#getString) | Crée java.lang.String en utilisant les points de code de ce cluster. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Crée java.lang.String en utilisant les points de code des clusters spécifiés. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Renvoie la largeur du cluster. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| points de code | int[] | Tableau de points Unicode composant un grapheme. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Tableau de [Glyph](../../com.aspose.words/glyph/) > composant un grapheme. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Renvoie un clone profond de cette instance.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Obtient les points de code du cluster.

**Returns:**
int[] - Points de code du cluster.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


Obtient le nombre total de points de code dans le [Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - Nombre total de points de code dans le [Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Obtient les glyphes du cluster.

**Returns:**
com.aspose.words.Glyph[] - Glyphes du cluster.
### getString() {#getString}
```
public String getString()
```


Crée java.lang.String en utilisant les points de code de ce cluster.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Crée java.lang.String en utilisant les points de code des clusters spécifiés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Renvoie la largeur du cluster.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
