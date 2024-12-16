---
title: FillType
linktitle: FillType
second_title: Aspose.Words for Java
description: Specifies fill type for a fillable object in Java.
type: docs
weight: 305
url: /java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Specifies fill type for a fillable object.

 **Examples:** 

Shows how to convert any of the fills back to solid fill.

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
## Fields

| Field | Description |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | Fill is the same as the background. |
| [GRADIENT](#GRADIENT) | Gradient fill. |
| [PATTERNED](#PATTERNED) | Patterned fill. |
| [PICTURE](#PICTURE) | Picture fill. |
| [SOLID](#SOLID) | Solid fill. |
| [TEXTURED](#TEXTURED) | Textured fill. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


Fill is the same as the background.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Gradient fill.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Patterned fill.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Picture fill.

### SOLID {#SOLID}
```
public static int SOLID
```


Solid fill.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Textured fill.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
