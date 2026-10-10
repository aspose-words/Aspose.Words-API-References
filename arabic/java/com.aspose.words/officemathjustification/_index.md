---
title: "OfficeMathJustification"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words لـ Java"
description: "يحدد محاذاة المعادلة في Java."
type: docs
weight: 498
url: /ar/java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

يحدد محاذاة المعادلة.

 **Examples:** 

يوضح كيفية تعيين تنسيق عرض الرياضيات المكتبية.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CENTER](#CENTER) | يُوسّط كل مثال من النص الرياضي بشكل فردي بالنسبة للهوامش. |
| [CENTER_GROUP](#CENTER-GROUP) | يُحاذي أمثلة النص الرياضي إلى اليسار بالنسبة لبعضها البعض، ويُوسّط مجموعة النص الرياضي (فقرة الرياضيات) بالنسبة للصفحة. |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | موضع Math المضمن. |
| [LEFT](#LEFT) | محاذاة اليسار لفقرة Math. |
| [RIGHT](#RIGHT) | محاذاة اليمين لفقرة Math. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


يُوسّط كل مثال من النص الرياضي بشكل فردي بالنسبة للهوامش.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


يُحاذي أمثلة النص الرياضي إلى اليسار بالنسبة لبعضها البعض، ويُوسّط مجموعة النص الرياضي (فقرة الرياضيات) بالنسبة للصفحة.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


موضع Math المضمن.

### LEFT {#LEFT}
```
public static int LEFT
```


محاذاة اليسار لفقرة Math.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


محاذاة اليمين لفقرة Math.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
