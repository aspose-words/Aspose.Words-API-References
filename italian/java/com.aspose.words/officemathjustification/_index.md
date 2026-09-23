---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento dell'equazione in Java."
type: docs
weight: 498
url: /it/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Specifica l'allineamento dell'equazione.

 **Examples:** 

Mostra come impostare la formattazione di visualizzazione della matematica di Office.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CENTER](#CENTER) | Centra ogni istanza di testo matematico individualmente rispetto ai margini. |
| [CENTER_GROUP](#CENTER-GROUP) | Allinea a sinistra le istanze di testo matematico rispetto l'una all'altra e centra il gruppo di testo matematico (il Paragrafo Matematico) rispetto alla pagina. |
| [DEFAULT](#DEFAULT) | Valore predefinito [CENTER\\_GROUP](../../com.aspose.words/officemathjustification/\\#CENTER-GROUP). |
| [INLINE](#INLINE) | Posizione in linea della Matematica. |
| [LEFT](#LEFT) | Allineamento a sinistra del Paragrafo Matematico. |
| [RIGHT](#RIGHT) | Allineamento a destra del Paragrafo Matematico. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Centra ogni istanza di testo matematico individualmente rispetto ai margini.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Allinea a sinistra le istanze di testo matematico rispetto l'una all'altra e centra il gruppo di testo matematico (il Paragrafo Matematico) rispetto alla pagina.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Valore predefinito [CENTER\\_GROUP](../../com.aspose.words/officemathjustification/\\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Posizione in linea della Matematica.

### LEFT {#LEFT}
```
public static int LEFT
```


Allineamento a sinistra del Paragrafo Matematico.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Allineamento a destra del Paragrafo Matematico.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
