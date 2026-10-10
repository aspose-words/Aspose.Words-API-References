---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words для Java"
description: "Указывает выравнивание уравнения в Java."
type: docs
weight: 498
url: /ru/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Указывает выравнивание уравнения.

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
| [CENTER](#CENTER) | Центрирует каждый отдельный фрагмент математического текста относительно полей. |
| [CENTER_GROUP](#CENTER-GROUP) | Выравнивает фрагменты математического текста по левому краю относительно друг друга и центрирует группу математического текста (параграф Math) относительно страницы. |
| [DEFAULT](#DEFAULT) | Значение по умолчанию [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | Встроенное положение Math. |
| [LEFT](#LEFT) | Выравнивание по левому краю параграфа Math. |
| [RIGHT](#RIGHT) | Выравнивание по правому краю параграфа Math. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Центрирует каждый отдельный фрагмент математического текста относительно полей.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Выравнивает фрагменты математического текста по левому краю относительно друг друга и центрирует группу математического текста (параграф Math) относительно страницы.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Значение по умолчанию [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Встроенное положение Math.

### LEFT {#LEFT}
```
public static int LEFT
```


Выравнивание по левому краю параграфа Math.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Выравнивание по правому краю параграфа Math.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int officeMathJustification) {#toString-int}
```
public static String toString(int officeMathJustification)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
