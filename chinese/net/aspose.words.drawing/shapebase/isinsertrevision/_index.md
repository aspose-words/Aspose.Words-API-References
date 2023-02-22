---
title: ShapeBase.IsInsertRevision
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 如果在启用更改跟踪时将此对象插入 Microsoft Word则返回 true
type: docs
weight: 290
url: /zh/net/aspose.words.drawing/shapebase/isinsertrevision/
---
## ShapeBase.IsInsertRevision property

如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

```csharp
public bool IsInsertRevision { get; }
```

### 例子

显示如何使用修订形状。

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// 插入一个内联形状而不跟踪修订，这将使该形状不是任何类型的修订。
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

// 因为我们在跟踪变化时移除了那个形状，
// 形状保留在文档中并算作删除修订。
// 接受此修订将永久删除形状，拒绝它将保留在文档中。
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// 我们在跟踪更改时插入了另一个形状，因此该形状将被视为插入修订。
// 接受这个修订将把这个形状作为非修订吸收到文档中，
// 拒绝修订将永久删除此形状。
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


