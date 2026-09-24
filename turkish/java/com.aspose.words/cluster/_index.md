---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words Java için"
description: "Java'da bir graphemi oluşturan kod noktalarını ve glifleri kapsüller."
type: docs
weight: 104
url: /tr/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

Bir grafemi oluşturan kod noktalarını ve glifleri kapsüller.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | Bu örneğin derin bir klonunu döndürür. |
| [getCodepoints()](#getCodepoints) | Kümenin kod noktalarını alır. |
| [getCodepointsLength()](#getCodepointsLength) | [Cluster](../../com.aspose.words/cluster/) içindeki toplam kod noktası sayısını alır. |
| [getGlyphs()](#getGlyphs) | Kümenin gliflerini alır. |
| [getString()](#getString) | Bu kümeden kod noktalarını kullanarak java.lang.String oluşturur. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | Belirtilen kümelerden kod noktalarını kullanarak java.lang.String oluşturur. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | Kümenin genişliğini döndürür. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| kod noktaları | int[] | Bir graphemi oluşturan Unicode noktalarının dizisi. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | Bir graphemi oluşturan [Glyph](../../com.aspose.words/glyph/) dizisi >. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


Bu örneğin derin bir klonunu döndürür.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


Kümenin kod noktalarını alır.

**Returns:**
int[] - Kümenin kod noktaları.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


[Cluster](../../com.aspose.words/cluster/) içindeki toplam kod noktası sayısını alır.

**Returns:**
int - [Cluster](../../com.aspose.words/cluster/) içindeki toplam kod noktası sayısı.
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


Kümenin gliflerini alır.

**Returns:**
com.aspose.words.Glyph[] - Kümenin glifleri.
### getString() {#getString}
```
public String getString()
```


Bu kümeden kod noktalarını kullanarak java.lang.String oluşturur.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


Belirtilen kümelerden kod noktalarını kullanarak java.lang.String oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


Kümenin genişliğini döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
