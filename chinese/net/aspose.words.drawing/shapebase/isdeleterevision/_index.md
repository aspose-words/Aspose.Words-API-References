---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words for .NET
description: 探索 ShapeBase IsDeleteRevision 属性，了解它如何在启用更改跟踪的情况下指示 Microsoft Word 中的对象删除，以增强文档管理。
type: docs
weight: 270
url: /zh/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。

```csharp
public bool IsDeleteRevision { get; }
```

## 例子

展示如何使用修订形状。

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// 插入一个不跟踪修订的内联形状，这将使该形状不再是任何类型的修订。
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// 开始跟踪修订，然后插入另一个形状，这将是一个修订。
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// 由于我们在跟踪变化时删除了该形状，
// 该形状在文档中保留并计为删除修订。
// 接受此修订将永久删除该形状，而拒绝此修订将将其保留在文档中。
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// 我们在跟踪变化的同时插入了另一个形状，因此该形状将算作插入修订。
// 接受此修订将把此形状作为非修订版本吸收到文档中，
// 并且拒绝修改将永久删除此形状。
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
