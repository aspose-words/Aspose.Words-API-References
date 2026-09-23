---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words für Java"
description: "Gibt die Ausrichtung der Gleichung in Java an."
type: docs
weight: 498
url: /de/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Gibt die Ausrichtung der Gleichung an.

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
| [CENTER](#CENTER) | Zentriert jede Instanz mathematischen Textes einzeln in Bezug auf die Ränder. |
| [CENTER_GROUP](#CENTER-GROUP) | Richtet Instanzen mathematischen Textes zueinander linksbündig aus und zentriert die Gruppe des mathematischen Textes (den Math-Absatz) in Bezug auf die Seite. |
| [DEFAULT](#DEFAULT) | Standardwert [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | Inline-Position von Math. |
| [LEFT](#LEFT) | Linksbündige Ausrichtung des Math-Absatzes. |
| [RIGHT](#RIGHT) | Rechtsbündige Ausrichtung des Math-Absatzes. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Zentriert jede Instanz mathematischen Textes einzeln in Bezug auf die Ränder.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Richtet Instanzen mathematischen Textes zueinander linksbündig aus und zentriert die Gruppe des mathematischen Textes (den Math-Absatz) in Bezug auf die Seite.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Inline-Position von Math.

### LEFT {#LEFT}
```
public static int LEFT
```


Linksbündige Ausrichtung des Math-Absatzes.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Rechtsbündige Ausrichtung des Math-Absatzes.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
