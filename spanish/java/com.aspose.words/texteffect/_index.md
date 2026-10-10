---
title: "TextEffect"
linktitle: "TextEffect"
second_title: "Aspose.Words para Java"
description: "Efecto de animación para ejecuciones de texto en Java."
type: docs
weight: 673
url: /es/java/com.aspose.words/texteffect/
---

**Inheritance:**
java.lang.Object
```
public class TextEffect
```

Efecto de animación para ejecuciones de texto.

 **Examples:** 

Muestra cómo aplicar un efecto visual a una ejecución.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BLINKING_BACKGROUND](#BLINKING-BACKGROUND) |  |
| [LAS_VEGAS_LIGHTS](#LAS-VEGAS-LIGHTS) |  |
| [MARCHING_BLACK_ANTS](#MARCHING-BLACK-ANTS) |  |
| [MARCHING_RED_ANTS](#MARCHING-RED-ANTS) |  |
| [NONE](#NONE) |  |
| [SHIMMER](#SHIMMER) |  |
| [SPARKLE_TEXT](#SPARKLE-TEXT) |  |
| [length](#length) |  |
## Métodos

| Método | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textEffect) {#getName-int}
```
public static String getName(int textEffect)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textEffect | int |  |

**Returns:**
java.lang.String
