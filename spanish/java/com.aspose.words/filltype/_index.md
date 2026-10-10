---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de relleno para un objeto rellenable en Java."
type: docs
weight: 312
url: /es/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Especifica el tipo de relleno para un objeto rellenable.

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | El relleno es el mismo que el fondo. |
| [GRADIENT](#GRADIENT) | Relleno degradado. |
| [PATTERNED](#PATTERNED) | Relleno con patrón. |
| [PICTURE](#PICTURE) | Relleno de imagen. |
| [SOLID](#SOLID) | Relleno sólido. |
| [TEXTURED](#TEXTURED) | Relleno texturizado. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


El relleno es el mismo que el fondo.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Relleno degradado.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Relleno con patrón.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Relleno de imagen.

### SOLID {#SOLID}
```
public static int SOLID
```


Relleno sólido.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Relleno texturizado.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
