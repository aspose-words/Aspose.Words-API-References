---
title: TextDmlEffect
linktitle: TextDmlEffect
second_title: Aspose.Words for Java
description: Dml text effect for text runs in Java.
type: docs
weight: 660
url: /java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Dml text effect for text runs.

 **Examples:** 

Shows how to check if a run displays a DrawingML text effect.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Fields

| Field | Description |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | 3D effect. |
| [FILL](#FILL) | Fill overlay effect. |
| [GLOW](#GLOW) | Glow effect, in which a color blurred outline is added outside the edges of the object. |
| [OUTLINE](#OUTLINE) | Outline effect. |
| [REFLECTION](#REFLECTION) | Reflection effect. |
| [SHADOW](#SHADOW) | Shadow effect. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


3D effect.

### FILL {#FILL}
```
public static int FILL
```


Fill overlay effect.

### GLOW {#GLOW}
```
public static int GLOW
```


Glow effect, in which a color blurred outline is added outside the edges of the object.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Outline effect.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Reflection effect.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Shadow effect.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
