---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase IsMoveToRevision 财产. 返回真的如果在启用更改跟踪的情况下在 Microsoft Word 中移动插入此对象 在 C#.
type: docs
weight: 330
url: /zh/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。

```csharp
public bool IsMoveToRevision { get; }
```

## 例子

展示如何识别移动修订形状。

```csharp
// 移动修订是指我们通过在 Microsoft Word 中剪切并粘贴来移动文档正文中的元素，同时
// 跟踪变化。如果我们在这样的文本移动中涉及内联形状，那么该形状也将是一个修订。
// 复制粘贴或移动浮动形状不会创建移动修订。
Document doc = new Document(MyDir + "Revision shape.docx");

// 移动修订由成对的“移自”和“移至”修订组成。我们以一种形式移入这份文件，
// 但在我们接受或拒绝移动修订之前，该形状将有两个实例。
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// 这是“移动到”修订版，这是其到达目的地的形状。
// 如果我们接受修订，这个“移动到”修订形状将会消失，
// 并且“移自”修订形状将保留。
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// 这是“移自”修订版，它是其原始位置的形状。
// 如果我们接受修订，这个“移自”修订形状将会消失，
// 并且“移至”修订形状将保留。
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
