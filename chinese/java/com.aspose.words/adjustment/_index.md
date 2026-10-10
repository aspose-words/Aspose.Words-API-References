---
title: "调整"
linktitle: "调整"
second_title: "Aspose.Words for Java"
description: "表示在 Java 中应用于指定形状的调整值。"
type: docs
weight: 11
url: /zh/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

表示应用于指定形状的调整值。

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
| [getName()](#getName) | 获取调整的名称。 |
| [getValue()](#getValue) | 获取调整的原始值。 |
| [setValue(int value)](#setValue-int) | 设置调整的原始值。 |
### getName() {#getName}
```
public String getName()
```


获取调整的名称。

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
java.lang.String - 调整的名称。
### getValue() {#getValue}
```
public int getValue()
```


获取调整的原始值。

 **Remarks:** 

调整值仅仅是一个具有基于数值公式的引导。也就是说，调整值引导本身不进行计算。相反，该引导指定一个参数值，用于形状引导内部的计算。

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
int - 调整的原始值。
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


设置调整的原始值。

 **Remarks:** 

调整值仅仅是一个具有基于数值公式的引导。也就是说，调整值引导本身不进行计算。相反，该引导指定一个参数值，用于形状引导内部的计算。

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
| value | int | 调整的原始值。 |

