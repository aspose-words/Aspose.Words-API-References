---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع التعبئة لكائن قابل للتعبئة في Java."
type: docs
weight: 312
url: /ar/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

يحدد نوع التعبئة لكائن قابل للتعبئة.

 **Examples:** 

يعرض كيفية تحويل أي من التعبئات إلى تعبئة صلبة.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | التعبئة هي نفسها الخلفية. |
| [GRADIENT](#GRADIENT) | تعبئة متدرجة. |
| [PATTERNED](#PATTERNED) | تعبئة بنمط. |
| [PICTURE](#PICTURE) | تعبئة صورة. |
| [SOLID](#SOLID) | تعبئة صلبة. |
| [TEXTURED](#TEXTURED) | تعبئة بنقش. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


التعبئة هي نفسها الخلفية.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


تعبئة متدرجة.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


تعبئة بنمط.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


تعبئة صورة.

### SOLID {#SOLID}
```
public static int SOLID
```


تعبئة صلبة.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


تعبئة بنقش.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
