---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words for .NET
description: 探索 Microsoft Word 中的 ShapeBase IsMoveFromRevision 属性。轻松追踪更改并精确识别已移动或删除的对象。
type: docs
weight: 340
url: /zh/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。

```csharp
public bool IsMoveFromRevision { get; }
```

## 例子

展示如何识别移动修订形状。

```csharp
// 移动修订是指我们在 Microsoft Word 中通过剪切粘贴来移动文档主体中的元素，同时
// 跟踪更改。如果我们在这样的文本移动中引入内联形状，那么该形状也将是一个修订。
// 复制粘贴或移动浮动形状不会创建移动修订。
Document doc = new Document(MyDir + "Revision shape.docx");

// 移动修订版本由“移动自”和“移动至”修订版本对组成。我们在此文档中移动了一个形状，
// 但直到我们接受或拒绝移动修订之前，该形状将会有两个实例。
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// 这是“移动到”修订版，即其到达目的地时的形状。
// 如果我们接受修订，则此“移至”修订形状将消失，
// 并且“从...移动”修订形状将保留。
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// 这是“从...移动”修订版，即其原始位置的形状。
// 如果我们接受修订，这个“从...移动”修订形状将会消失，
// 并且“移动到”修订形状将保留。
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
