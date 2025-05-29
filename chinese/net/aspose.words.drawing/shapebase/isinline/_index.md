---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words for .NET
description: 探索 ShapeBase IsInline 属性，轻松检查形状是否与文本对齐，增强设计并提高布局效率。
type: docs
weight: 310
url: /zh/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

快速确定此形状是否与文本对齐。

```csharp
public bool IsInline { get; }
```

## 评论

仅对顶层形状有效。

## 例子

展示如何确定形状是内联的还是浮动的。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是形状可能具有的两种包装类型。
// 1 - 内联：
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// 内联形状位于段落内，与其他段落元素（例如文本）相邻。
// 在 Microsoft Word 中，我们可以单击并将形状拖动到任何段落，就像它是一个字符一样。
// 如果形状很大，它会影响垂直段落间距。
// 我们不能将此形状移动到没有段落的地方。
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - 浮动：
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// 浮动形状属于我们将其插入到的段落，
// 我们可以通过单击形状时出现的锚符号来确定。
// 如果形状左侧没有可见的锚符号，
// 我们需要通过“选项”->“显示”->“对象锚点”启用可见锚点。
// 在 Microsoft Word 中，我们可以单击鼠标左键并拖动此形状到任意位置。
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
