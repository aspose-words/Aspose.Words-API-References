---
title: "OfficeMathDisplayType"
linktitle: "OfficeMathDisplayType"
second_title: "Aspose.Words для Java"
description: "Указывает тип формата отображения уравнения в Java."
type: docs
weight: 497
url: /ru/java/com.aspose.words/officemathdisplaytype/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathDisplayType
```

Указывает тип формата отображения уравнения.

 **Examples:** 

Показывает, как задать формат отображения офисных формул.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // OfficeMath nodes that are children of other OfficeMath nodes are always inline.
 // The node we are working with is the base node to change its location and display type.
 Assert.assertEquals(MathObjectType.O_MATH_PARA, officeMath.getMathObjectType());
 Assert.assertEquals(NodeType.OFFICE_MATH, officeMath.getNodeType());
 Assert.assertEquals(officeMath.getParentNode(), officeMath.getParentParagraph());

 // Change the location and display type of the OfficeMath node.
 officeMath.setDisplayType(OfficeMathDisplayType.DISPLAY);
 officeMath.setJustification(OfficeMathJustification.LEFT);

 doc.save(getArtifactsDir() + "Shape.OfficeMath.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DISPLAY](#DISPLAY) | Office Math отображается на отдельной строке. |
| [INLINE](#INLINE) | Элемент Office Math отображается встроенно в текст. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String officeMathDisplayTypeName)](#fromName-java.lang.String) |  |
| [getName(int officeMathDisplayType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathDisplayType)](#toString-int) |  |
### DISPLAY {#DISPLAY}
```
public static int DISPLAY
```


Office Math отображается на отдельной строке.

### INLINE {#INLINE}
```
public static int INLINE
```


Элемент Office Math отображается встроенно в текст.

### length {#length}
```
public static int length
```


### fromName(String officeMathDisplayTypeName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathDisplayTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMathDisplayTypeName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathDisplayType) {#getName-int}
```
public static String getName(int officeMathDisplayType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMathDisplayType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int officeMathDisplayType) {#toString-int}
```
public static String toString(int officeMathDisplayType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMathDisplayType | int |  |

**Returns:**
java.lang.String
