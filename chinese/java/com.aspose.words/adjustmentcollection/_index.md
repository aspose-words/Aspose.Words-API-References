---
title: "AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words for Java"
description: "表示一个只读集合，其中包含在 Java 中应用于指定形状的 Adjustment 调整值。"
type: docs
weight: 12
url: /zh/java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

表示一个只读集合，其中包含应用于指定形状的 [Adjustment](../../com.aspose.words/adjustment/) 调整值。

 **Examples:** 

展示如何使用调整原始值。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [get(int index)](#get-int) | 返回指定索引处的 adjustment。 |
| [getCount()](#getCount) | 获取集合中包含的元素数量。 |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


返回指定索引处的 adjustment。

 **Examples:** 

展示如何使用调整原始值。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int | 集合中的索引。 |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


获取集合中包含的元素数量。

 **Examples:** 

展示如何使用调整原始值。

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
int - 集合中包含的元素数量。
