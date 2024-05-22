---
title: AdjustmentCollection
linktitle: AdjustmentCollection
second_title: Aspose.Words for Java
description: Represents a read-only collection of Adjustment adjust values that are applied to the specified shape in Java.
type: docs
weight: 12
url: /java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

Represents a read-only collection of [Adjustment](../../com.aspose.words/adjustment/) adjust values that are applied to the specified shape.

 **Examples:** 

Shows how to work with adjustment raw values.

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
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Returns an adjustment at the specified index. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


Returns an adjustment at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
