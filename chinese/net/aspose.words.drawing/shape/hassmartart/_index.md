---
title: Shape.HasSmartArt
second_title: Aspose.Words for .NET API 参考
description: Shape 财产. 如果此 Shape 具有 SmartArt 对象则返回 true
type: docs
weight: 90
url: /zh/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

如果此 Shape 具有 SmartArt 对象，则返回 true。

```csharp
public bool HasSmartArt { get; }
```

### 例子

演示如何使用 SmartArt 对象计算文档中形状的数量。

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### 也可以看看

* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../shape/)
* 部件 [Aspose.Words](../../../)


