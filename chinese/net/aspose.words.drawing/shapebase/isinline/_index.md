---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase IsInline 财产. 确定此形状是否与文本内联放置的快速方法 在 C#.
type: docs
weight: 290
url: /zh/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

确定此形状是否与文本内联放置的快速方法。

```csharp
public bool IsInline { get; }
```

## 评论

仅对顶级形状有效。

## 例子

演示如何确定形状是内联形状还是浮动形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是形状可能具有的两种环绕类型。
// 1 - 内联：
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// 内联形状位于段落内的其他段落元素中，例如文本串。
// 在 Microsoft Word 中，我们可以单击形状并将其拖动到任何段落，就像它是一个字符一样。
// 如果形状较大，会影响垂直段落间距。
// 我们不能将这个形状移动到没有段落的地方。
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - 浮动：
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// 浮动形状属于我们将其插入的段落，
// 我们可以通过单击形状时出现的锚符号来确定。
// 如果形状的左侧没有可见的锚符号，
// 我们需要通过“选项”启用可见锚点 -> 「显示」-> “对象锚”。
// 在Microsoft Word中，我们可以左键单击此形状并将其自由拖动到任何位置。
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
