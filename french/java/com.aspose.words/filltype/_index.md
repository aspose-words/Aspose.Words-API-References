---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de remplissage pour un objet remplissable en Java."
type: docs
weight: 312
url: /fr/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Spécifie le type de remplissage pour un objet remplissable.

 **Examples:** 

Montre comment convertir n'importe quel remplissage en remplissage uni.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | Le remplissage est identique à l'arrière-plan. |
| [GRADIENT](#GRADIENT) | Remplissage en dégradé. |
| [PATTERNED](#PATTERNED) | Remplissage à motif. |
| [PICTURE](#PICTURE) | Remplissage d'image. |
| [SOLID](#SOLID) | Remplissage uni. |
| [TEXTURED](#TEXTURED) | Remplissage texturé. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


Le remplissage est identique à l'arrière-plan.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Remplissage en dégradé.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Remplissage à motif.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Remplissage d'image.

### SOLID {#SOLID}
```
public static int SOLID
```


Remplissage uni.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Remplissage texturé.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fillType) {#toString-int}
```
public static String toString(int fillType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
