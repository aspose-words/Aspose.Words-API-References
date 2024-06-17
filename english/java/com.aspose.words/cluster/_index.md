---
title: Cluster
linktitle: Cluster
second_title: Aspose.Words for Java
description: Encapsulates code points and glyphs composing a grapheme in Java.
type: docs
weight: 96
url: /java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Encapsulates code points and glyphs composing a grapheme.
## Constructors

| Constructor | Description |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Initializes new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [deepClone()](#deepClone) | Returns a deep clone of this instance. |
| [getCodepoints()](#getCodepoints) | Gets codepoints of the cluster. |
| [getCodepointsLength()](#getCodepointsLength) | Gets total number of codepoints in the [Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | Gets glyphs of the cluster. |
| [getString()](#getString) | Creates java.lang.String using codepoints from this cluster. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Creates java.lang.String using codepoints from the specified clusters. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Returns width of the cluster. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Initializes new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| codepoints | int[] | Array of Unicode points composing a grapheme. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Array of [Glyph](../../com.aspose.words/glyph/) > composing a grapheme. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Returns a deep clone of this instance.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Gets codepoints of the cluster.

**Returns:**
int[] - Codepoints of the cluster.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


Gets total number of codepoints in the [Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - Total number of codepoints in the [Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Gets glyphs of the cluster.

**Returns:**
com.aspose.words.Glyph[] - Glyphs of the cluster.
### getString() {#getString}
```
public String getString()
```


Creates java.lang.String using codepoints from this cluster.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Creates java.lang.String using codepoints from the specified clusters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Returns width of the cluster.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
