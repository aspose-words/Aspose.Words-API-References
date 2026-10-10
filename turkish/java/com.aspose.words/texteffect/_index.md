---
title: "TextEffect"
linktitle: "TextEffect"
second_title: "Aspose.Words Java için"
description: "Java'da metin akışları için animasyon efekti."
type: docs
weight: 673
url: /tr/java/com.aspose.words/texteffect/
---

**Inheritance:**
java.lang.Object
```
public class TextEffect
```

Metin akışları için animasyon efekti.

 **Examples:** 

Bir akışa görsel bir efekt nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BLINKING_BACKGROUND](#BLINKING-BACKGROUND) |  |
| [LAS_VEGAS_LIGHTS](#LAS-VEGAS-LIGHTS) |  |
| [MARCHING_BLACK_ANTS](#MARCHING-BLACK-ANTS) |  |
| [MARCHING_RED_ANTS](#MARCHING-RED-ANTS) |  |
| [NONE](#NONE) |  |
| [SHIMMER](#SHIMMER) |  |
| [SPARKLE_TEXT](#SPARKLE-TEXT) |  |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textEffectName)](#fromName-java.lang.String) |  |
| [getName(int textEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textEffect)](#toString-int) |  |
### BLINKING_BACKGROUND {#BLINKING-BACKGROUND}
```
public static int BLINKING_BACKGROUND
```




### LAS_VEGAS_LIGHTS {#LAS-VEGAS-LIGHTS}
```
public static int LAS_VEGAS_LIGHTS
```




### MARCHING_BLACK_ANTS {#MARCHING-BLACK-ANTS}
```
public static int MARCHING_BLACK_ANTS
```




### MARCHING_RED_ANTS {#MARCHING-RED-ANTS}
```
public static int MARCHING_RED_ANTS
```




### NONE {#NONE}
```
public static int NONE
```




### SHIMMER {#SHIMMER}
```
public static int SHIMMER
```




### SPARKLE_TEXT {#SPARKLE-TEXT}
```
public static int SPARKLE_TEXT
```




### length {#length}
```
public static int length
```


### fromName(String textEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textEffectName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textEffect) {#getName-int}
```
public static String getName(int textEffect)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textEffect | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textEffect) {#toString-int}
```
public static String toString(int textEffect)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textEffect | int |  |

**Returns:**
java.lang.String
