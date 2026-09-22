---
title: "Adjustment"
linktitle: "Adjustment"
second_title: "Aspose.Words لـ Java"
description: "يمثل قيم التعديل التي تُطبق على الشكل المحدد في Java."
type: docs
weight: 11
url: /ar/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

يمثل قيم التعديل التي تُطبق على الشكل المحدد.

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
| [getName()](#getName) | يحصل على اسم التعديل. |
| [getValue()](#getValue) | يحصل على القيمة الخام للتعديل. |
| [setValue(int value)](#setValue-int) | يضبط القيمة الخام للتعديل. |
### getName() {#getName}
```
public String getName()
```


يحصل على اسم التعديل.

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
java.lang.String - اسم التعديل.
### getValue() {#getValue}
```
public int getValue()
```


يحصل على القيمة الخام للتعديل.

 **Remarks:** 

قيمة التعديل هي ببساطة دليل يحتوي على صيغة مستندة إلى قيمة محددة. أي أنه لا يتم إجراء أي حساب لقيمة دليل التعديل. بدلاً من ذلك، يحدد هذا الدليل قيمة معلمة تُستخدم في الحسابات داخل أدلة الشكل.

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
int - القيمة الخام للتعديل.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


يضبط القيمة الخام للتعديل.

 **Remarks:** 

قيمة التعديل هي ببساطة دليل يحتوي على صيغة مستندة إلى قيمة محددة. أي أنه لا يتم إجراء أي حساب لقيمة دليل التعديل. بدلاً من ذلك، يحدد هذا الدليل قيمة معلمة تُستخدم في الحسابات داخل أدلة الشكل.

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
| قيمة | int | القيمة الخام للتعديل. |

