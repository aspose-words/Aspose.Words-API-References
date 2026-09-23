---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'alignement de l'équation en Java."
type: docs
weight: 498
url: /fr/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Spécifie l'alignement de l'équation.

 **Examples:** 

Montre comment définir le format d'affichage des mathématiques de bureau.

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
## Champs

| Champ | Description |
| --- | --- |
| [CENTER](#CENTER) | Centre chaque instance de texte mathématique individuellement par rapport aux marges. |
| [CENTER_GROUP](#CENTER-GROUP) | Aligne à gauche les instances de texte mathématique les unes par rapport aux autres, et centre le groupe de texte mathématique (le paragraphe Math) par rapport à la page. |
| [DEFAULT](#DEFAULT) | Valeur par défaut [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | Position en ligne des mathématiques. |
| [LEFT](#LEFT) | Alignement à gauche du paragraphe Math. |
| [RIGHT](#RIGHT) | Alignement à droite du paragraphe Math. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Centre chaque instance de texte mathématique individuellement par rapport aux marges.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Aligne à gauche les instances de texte mathématique les unes par rapport aux autres, et centre le groupe de texte mathématique (le paragraphe Math) par rapport à la page.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Valeur par défaut [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Position en ligne des mathématiques.

### LEFT {#LEFT}
```
public static int LEFT
```


Alignement à gauche du paragraphe Math.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Alignement à droite du paragraphe Math.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
