---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words para Java"
description: "Especifica la justificación de la ecuación en Java."
type: docs
weight: 498
url: /es/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Especifica la justificación de la ecuación.

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
| [CENTER](#CENTER) | Centra cada instancia de texto matemático individualmente con respecto a los márgenes. |
| [CENTER_GROUP](#CENTER-GROUP) | Justifica las instancias de texto matemático a la izquierda con respecto a cada una, y centra el grupo de texto matemático (el Párrafo Matemático) con respecto a la página. |
| [DEFAULT](#DEFAULT) | Valor predeterminado [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | Posición en línea de Math. |
| [LEFT](#LEFT) | Justificación izquierda del Párrafo Math. |
| [RIGHT](#RIGHT) | Justificación derecha del Párrafo Math. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Centra cada instancia de texto matemático individualmente con respecto a los márgenes.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Justifica las instancias de texto matemático a la izquierda con respecto a cada una, y centra el grupo de texto matemático (el Párrafo Matemático) con respecto a la página.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Valor predeterminado [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Posición en línea de Math.

### LEFT {#LEFT}
```
public static int LEFT
```


Justificación izquierda del Párrafo Math.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Justificación derecha del Párrafo Math.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
