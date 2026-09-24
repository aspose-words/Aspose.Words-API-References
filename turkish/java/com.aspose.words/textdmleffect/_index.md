---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words Java için"
description: "Java'da metin çalıştırmaları için Dml metin efekti."
type: docs
weight: 672
url: /tr/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Metin akışları için Dml metin efekti.

 **Examples:** 

Bir çalıştırmanın DrawingML metin efekti gösterip göstermediğini nasıl kontrol edeceğini gösterir.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | 3D efekti. |
| [FILL](#FILL) | Dolgu bindirme efekti. |
| [GLOW](#GLOW) | Parıltı efekti, nesnenin kenarlarının dışına renkli bulanık bir kontur eklenir. |
| [OUTLINE](#OUTLINE) | Kontur efekti. |
| [REFLECTION](#REFLECTION) | Yansıma efekti. |
| [SHADOW](#SHADOW) | Gölge efekti. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


3D efekti.

### FILL {#FILL}
```
public static int FILL
```


Dolgu bindirme efekti.

### GLOW {#GLOW}
```
public static int GLOW
```


Parıltı efekti, nesnenin kenarlarının dışına renkli bulanık bir kontur eklenir.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Kontur efekti.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Yansıma efekti.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Gölge efekti.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textDmlEffect) {#toString-int}
```
public static String toString(int textDmlEffect)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
