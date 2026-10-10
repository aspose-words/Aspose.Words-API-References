---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words für Java"
description: "Dml-Text-Effekt für Textläufe in Java."
type: docs
weight: 672
url: /de/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Dml-Texteffekt für Textläufe.

 **Examples:** 

Zeigt, wie überprüft wird, ob ein Lauf einen DrawingML-Text-Effekt anzeigt.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | 3D-Effekt. |
| [FILL](#FILL) | Füllüberlagerungs-Effekt. |
| [GLOW](#GLOW) | Leuchteffekt, bei dem eine farbige, verschwommene Kontur außerhalb der Kanten des Objekts hinzugefügt wird. |
| [OUTLINE](#OUTLINE) | Umriss‑Effekt. |
| [REFLECTION](#REFLECTION) | Spiegelungseffekt. |
| [SHADOW](#SHADOW) | Schatteneffekt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


3D-Effekt.

### FILL {#FILL}
```
public static int FILL
```


Füllüberlagerungs-Effekt.

### GLOW {#GLOW}
```
public static int GLOW
```


Leuchteffekt, bei dem eine farbige, verschwommene Kontur außerhalb der Kanten des Objekts hinzugefügt wird.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Umriss‑Effekt.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Spiegelungseffekt.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Schatteneffekt.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
