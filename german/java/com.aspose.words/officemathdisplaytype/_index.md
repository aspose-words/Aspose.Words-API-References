---
title: "OfficeMathDisplayType"
linktitle: "OfficeMathDisplayType"
second_title: "Aspose.Words für Java"
description: "Gibt den Anzeigetyp des Formats der Gleichung in Java an."
type: docs
weight: 497
url: /de/java/com.aspose.words/officemathdisplaytype/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathDisplayType
```

Gibt den Anzeigetyp des Gleichungsformats an.

 **Examples:** 

Zeigt, wie die Anzeigeformatierung für Office-Mathematik festgelegt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DISPLAY](#DISPLAY) | Das Office Math wird in einer eigenen Zeile angezeigt. |
| [INLINE](#INLINE) | Das Office Math wird im Textfluss angezeigt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String officeMathDisplayTypeName)](#fromName-java.lang.String) |  |
| [getName(int officeMathDisplayType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathDisplayType)](#toString-int) |  |
### DISPLAY {#DISPLAY}
```
public static int DISPLAY
```


Das Office Math wird in einer eigenen Zeile angezeigt.

### INLINE {#INLINE}
```
public static int INLINE
```


Das Office Math wird im Textfluss angezeigt.

### length {#length}
```
public static int length
```


### fromName(String officeMathDisplayTypeName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathDisplayTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| officeMathDisplayTypeName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathDisplayType) {#getName-int}
```
public static String getName(int officeMathDisplayType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| officeMathDisplayType | int |  |

**Returns:**
java.lang.String
