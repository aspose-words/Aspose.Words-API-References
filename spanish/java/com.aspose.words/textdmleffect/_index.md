---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words para Java"
description: "Efecto de texto Dml para ejecuciones de texto en Java."
type: docs
weight: 672
url: /es/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Efecto de texto Dml para ejecuciones de texto.

 **Examples:** 

Muestra cómo comprobar si una ejecución muestra un efecto de texto DrawingML.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | Efecto 3D. |
| [FILL](#FILL) | Efecto de superposición de relleno. |
| [GLOW](#GLOW) | Efecto de resplandor, en el que se agrega un contorno borroso de color fuera de los bordes del objeto. |
| [OUTLINE](#OUTLINE) | Efecto de contorno. |
| [REFLECTION](#REFLECTION) | Efecto de reflejo. |
| [SHADOW](#SHADOW) | Efecto de sombra. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


Efecto 3D.

### FILL {#FILL}
```
public static int FILL
```


Efecto de superposición de relleno.

### GLOW {#GLOW}
```
public static int GLOW
```


Efecto de resplandor, en el que se agrega un contorno borroso de color fuera de los bordes del objeto.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Efecto de contorno.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Efecto de reflejo.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Efecto de sombra.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
