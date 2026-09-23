---
title: "OfficeMathDisplayType"
linktitle: "OfficeMathDisplayType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di formato di visualizzazione dell'equazione in Java."
type: docs
weight: 497
url: /it/java/com.aspose.words/officemathdisplaytype/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathDisplayType
```

Specifica il tipo di formato di visualizzazione dell'equazione.

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
| [DISPLAY](#DISPLAY) | L'Office Math viene visualizzato su una propria riga. |
| [INLINE](#INLINE) | L'Office Math è visualizzato in linea con il testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String officeMathDisplayTypeName)](#fromName-java.lang.String) |  |
| [getName(int officeMathDisplayType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathDisplayType)](#toString-int) |  |
### DISPLAY {#DISPLAY}
```
public static int DISPLAY
```


L'Office Math viene visualizzato su una propria riga.

### INLINE {#INLINE}
```
public static int INLINE
```


L'Office Math è visualizzato in linea con il testo.

### length {#length}
```
public static int length
```


### fromName(String officeMathDisplayTypeName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathDisplayTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| officeMathDisplayTypeName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathDisplayType) {#getName-int}
```
public static String getName(int officeMathDisplayType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| officeMathDisplayType | int |  |

**Returns:**
java.lang.String
