---
title: "Cluster"
linktitle: "Cluster"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على نقاط الشيفرة والرموز التي تشكل وحدة كتابة في Java."
type: docs
weight: 104
url: /ar/java/com.aspose.words/cluster/
---

**Inheritance:**
java.lang.Object
```
public class Cluster
```

يحتوي على نقاط الشيفرة والرموز التي تشكل وحدة كتابة.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [Cluster(int[] codepoints, Glyph[] glyphs)](#Cluster-int---com.aspose.words.Glyph) | يُهيئ نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | يعيد نسخة عميقة من هذا المثيل. |
| [getCodepoints()](#getCodepoints) | يحصل على نقاط الشيفرة للـCluster. |
| [getCodepointsLength()](#getCodepointsLength) | يحصل على العدد الإجمالي لنقاط الشيفرة في الـ[Cluster](../../com.aspose.words/cluster/). |
| [getGlyphs()](#getGlyphs) | يحصل على الرموز للـCluster. |
| [getString()](#getString) | ينشئ java.lang.String باستخدام نقاط الشيفرة من هذا الـCluster. |
| [getString(Cluster[] clusters)](#getString-com.aspose.words.Cluster) | ينشئ java.lang.String باستخدام نقاط الشيفرة من الـclusters المحددة. |
| [getWidth(int em, float fontSize)](#getWidth-int-float) | يعيد عرض الـCluster. |
### Cluster(int[] codepoints, Glyph[] glyphs) {#Cluster-int---com.aspose.words.Glyph}
```
public Cluster(int[] codepoints, Glyph[] glyphs)
```


يُهيئ نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نقاط الشيفرة | int[] | مصفوفة من نقاط Unicode التي تشكل وحدة كتابة. |
| glyphs | [Glyph\[\]](../../com.aspose.words/glyph/) | مصفوفة من [Glyph](../../com.aspose.words/glyph/) > التي تشكل وحدة كتابة. |

### deepClone() {#deepClone}
```
public Cluster deepClone()
```


يعيد نسخة عميقة من هذا المثيل.

**Returns:**
[Cluster](../../com.aspose.words/cluster/)
### getCodepoints() {#getCodepoints}
```
public int[] getCodepoints()
```


يحصل على نقاط الشيفرة للـCluster.

**Returns:**
int[] - نقاط الشيفرة للـCluster.
### getCodepointsLength() {#getCodepointsLength}
```
public int getCodepointsLength()
```


يحصل على العدد الإجمالي لنقاط الشيفرة في الـ[Cluster](../../com.aspose.words/cluster/).

**Returns:**
int - العدد الإجمالي لنقاط الشيفرة في الـ[Cluster](../../com.aspose.words/cluster/).
### getGlyphs() {#getGlyphs}
```
public Glyph[] getGlyphs()
```


يحصل على الرموز للـCluster.

**Returns:**
com.aspose.words.Glyph[] - الرموز للـCluster.
### getString() {#getString}
```
public String getString()
```


ينشئ java.lang.String باستخدام نقاط الشيفرة من هذا الـCluster.

**Returns:**
java.lang.String
### getString(Cluster[] clusters) {#getString-com.aspose.words.Cluster}
```
public static String getString(Cluster[] clusters)
```


ينشئ java.lang.String باستخدام نقاط الشيفرة من الـclusters المحددة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| clusters | [Cluster\[\]](../../com.aspose.words/cluster/) |  |

**Returns:**
java.lang.String
### getWidth(int em, float fontSize) {#getWidth-int-float}
```
public float getWidth(int em, float fontSize)
```


يعيد عرض الـCluster.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| em | int |  |
| fontSize | float |  |

**Returns:**
float
