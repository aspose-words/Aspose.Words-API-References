---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words для Java"
description: "Указывает тип заливки для заполняемого объекта в Java."
type: docs
weight: 312
url: /ru/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Указывает тип заполнения для заполняемого объекта.

 **Examples:** 

Показывает, как преобразовать любую из заливок обратно в сплошную заливку.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | Заливка совпадает с фоном. |
| [GRADIENT](#GRADIENT) | Градиентная заливка. |
| [PATTERNED](#PATTERNED) | Заливка узором. |
| [PICTURE](#PICTURE) | Заливка изображением. |
| [SOLID](#SOLID) | Сплошная заливка. |
| [TEXTURED](#TEXTURED) | Текстурированная заливка. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


Заливка совпадает с фоном.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Градиентная заливка.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Заливка узором.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Заливка изображением.

### SOLID {#SOLID}
```
public static int SOLID
```


Сплошная заливка.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Текстурированная заливка.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
