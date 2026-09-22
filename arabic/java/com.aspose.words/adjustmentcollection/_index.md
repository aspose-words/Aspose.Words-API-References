---
title: "AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة قراءة فقط من قيم تعديل Adjustment التي تُطبق على الشكل المحدد في Java."
type: docs
weight: 12
url: /ar/java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

يمثل مجموعة للقراءة فقط من قيم [Adjustment](../../com.aspose.words/adjustment/) التي تُطبق على الشكل المحدد.

 **Examples:** 

يوضح كيفية العمل مع القيم الأولية للتعديل.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يعيد تعديلًا في الفهرس المحدد. |
| [getCount()](#getCount) | يحصل على عدد العناصر الموجودة في المجموعة. |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


يعيد تعديلًا في الفهرس المحدد.

 **Examples:** 

يوضح كيفية العمل مع القيم الأولية للتعديل.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس داخل المجموعة. |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد العناصر الموجودة في المجموعة.

 **Examples:** 

يوضح كيفية العمل مع القيم الأولية للتعديل.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Returns:**
int - عدد العناصر الموجودة في المجموعة.
