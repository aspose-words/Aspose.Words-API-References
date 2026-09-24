---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words Java için"
description: "Java'da denklemin hizalamasını belirtir."
type: docs
weight: 498
url: /tr/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Denklemin hizalamasını belirtir.

 **Examples:** 

Office math görüntüleme biçimlendirmesinin nasıl ayarlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CENTER](#CENTER) | Matematiksel metnin her örneğini kenarlara göre ayrı ayrı ortalar. |
| [CENTER_GROUP](#CENTER-GROUP) | Matematiksel metin örneklerini birbirine göre sola hizalar ve Math Paragraph'ı sayfaya göre ortalar. |
| [DEFAULT](#DEFAULT) | Varsayılan değer [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | Math'in satır içi konumu. |
| [LEFT](#LEFT) | Math Paragraph'ın sola hizalanması. |
| [RIGHT](#RIGHT) | Math Paragraph'ın sağa hizalanması. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Matematiksel metnin her örneğini kenarlara göre ayrı ayrı ortalar.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Matematiksel metin örneklerini birbirine göre sola hizalar ve Math Paragraph'ı sayfaya göre ortalar.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Math'in satır içi konumu.

### LEFT {#LEFT}
```
public static int LEFT
```


Math Paragraph'ın sola hizalanması.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Math Paragraph'ın sağa hizalanması.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
