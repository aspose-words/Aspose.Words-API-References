---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words for .NET
description: 通过 HasSmartArt 属性，了解你的 Shape 是否包含 SmartArt 对象。为你的项目解锁更多创意设计可能性！
type: docs
weight: 100
url: /zh/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

返回`真的`如果这个[`Shape`](../)有一个 SmartArt 对象。

```csharp
public bool HasSmartArt { get; }
```

## 例子

展示如何使用 SmartArt 对象计算文档中形状的数量。

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### 也可以看看

* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
