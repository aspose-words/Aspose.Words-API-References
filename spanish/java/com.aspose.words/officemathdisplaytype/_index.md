---
title: "OfficeMathDisplayType"
linktitle: "OfficeMathDisplayType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de formato de visualización de la ecuación en Java."
type: docs
weight: 497
url: /es/java/com.aspose.words/officemathdisplaytype/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathDisplayType
```

Especifica el tipo de formato de visualización de la ecuación.

 **Examples:** 

Muestra cómo establecer el formato de visualización de office math.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DISPLAY](#DISPLAY) | El Office Math se muestra en una línea propia. |
| [INLINE](#INLINE) | El Office Math se muestra en línea con el texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String officeMathDisplayTypeName)](#fromName-java.lang.String) |  |
| [getName(int officeMathDisplayType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathDisplayType)](#toString-int) |  |
### DISPLAY {#DISPLAY}
```
public static int DISPLAY
```


El Office Math se muestra en una línea propia.

### INLINE {#INLINE}
```
public static int INLINE
```


El Office Math se muestra en línea con el texto.

### length {#length}
```
public static int length
```


### fromName(String officeMathDisplayTypeName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathDisplayTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| officeMathDisplayTypeName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathDisplayType) {#getName-int}
```
public static String getName(int officeMathDisplayType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| officeMathDisplayType | int |  |

**Returns:**
java.lang.String
