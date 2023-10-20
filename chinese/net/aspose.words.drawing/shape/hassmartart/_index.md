---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: 用于 .NET 的 Aspose.Words
description: Shape HasSmartArt 财产. 返回真的如果这Shape有一个 SmartArt 对象 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

返回`真的`如果这[`Shape`](../)有一个 SmartArt 对象。

```csharp
public bool HasSmartArt { get; }
```

## 例子

演示如何计算文档中包含 SmartArt 对象的形状数量。

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### 也可以看看

* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
