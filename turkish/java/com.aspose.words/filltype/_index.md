---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words Java için"
description: "Java'da doldurulabilir bir nesne için dolgu tipini belirtir."
type: docs
weight: 312
url: /tr/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Doldurulabilir bir nesne için dolgu tipini belirtir.

 **Examples:** 

Herhangi bir doldurmanın katı doldurmaya nasıl dönüştürüleceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | Dolgu, arka plan ile aynıdır. |
| [GRADIENT](#GRADIENT) | Gradyan dolgu. |
| [PATTERNED](#PATTERNED) | Desenli dolgu. |
| [PICTURE](#PICTURE) | Resim dolgu. |
| [SOLID](#SOLID) | Katı dolgu. |
| [TEXTURED](#TEXTURED) | Doku dolgu. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


Dolgu, arka plan ile aynıdır.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Gradyan dolgu.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Desenli dolgu.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Resim dolgu.

### SOLID {#SOLID}
```
public static int SOLID
```


Katı dolgu.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Doku dolgu.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
