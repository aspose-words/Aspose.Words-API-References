---
title: "TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Aspose.Words pour Java"
description: "Effet de texte Dml pour les exécutions de texte en Java."
type: docs
weight: 672
url: /fr/java/com.aspose.words/textdmleffect/
---

**Inheritance:**
java.lang.Object
```
public class TextDmlEffect
```

Effet de texte Dml pour les séquences de texte.

 **Examples:** 

Montre comment vérifier si une exécution affiche un effet de texte DrawingML.

```

 Document doc = new Document(getMyDir() + "DrawingML text effects.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertTrue(runs.get(0).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(1).getFont().hasDmlEffect(TextDmlEffect.SHADOW));
 Assert.assertTrue(runs.get(2).getFont().hasDmlEffect(TextDmlEffect.REFLECTION));
 Assert.assertTrue(runs.get(3).getFont().hasDmlEffect(TextDmlEffect.EFFECT_3_D));
 Assert.assertTrue(runs.get(4).getFont().hasDmlEffect(TextDmlEffect.FILL));
 
```
## Champs

| Champ | Description |
| --- | --- |
| [EFFECT_3_D](#EFFECT-3-D) | Effet 3D. |
| [FILL](#FILL) | Effet de superposition de remplissage. |
| [GLOW](#GLOW) | Effet de lueur, dans lequel un contour flou coloré est ajouté à l'extérieur des bords de l'objet. |
| [OUTLINE](#OUTLINE) | Effet de contour. |
| [REFLECTION](#REFLECTION) | Effet de réflexion. |
| [SHADOW](#SHADOW) | Effet d'ombre. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String textDmlEffectName)](#fromName-java.lang.String) |  |
| [getName(int textDmlEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textDmlEffect)](#toString-int) |  |
### EFFECT_3_D {#EFFECT-3-D}
```
public static int EFFECT_3_D
```


Effet 3D.

### FILL {#FILL}
```
public static int FILL
```


Effet de superposition de remplissage.

### GLOW {#GLOW}
```
public static int GLOW
```


Effet de lueur, dans lequel un contour flou coloré est ajouté à l'extérieur des bords de l'objet.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Effet de contour.

### REFLECTION {#REFLECTION}
```
public static int REFLECTION
```


Effet de réflexion.

### SHADOW {#SHADOW}
```
public static int SHADOW
```


Effet d'ombre.

### length {#length}
```
public static int length
```


### fromName(String textDmlEffectName) {#fromName-java.lang.String}
```
public static int fromName(String textDmlEffectName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| textDmlEffectName | java.lang.String |  |

**Returns:**
int
### getName(int textDmlEffect) {#getName-int}
```
public static String getName(int textDmlEffect)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| textDmlEffect | int |  |

**Returns:**
java.lang.String
