---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase AnchorLocked 财产. 指定形状的锚点是否被锁定 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

指定形状的锚点是否被锁定。

```csharp
public bool AnchorLocked { get; set; }
```

## 评论

默认值为`错误的`。

仅对顶级形状有效。

此属性会影响 Microsoft Word 中形状锚点的行为。 当锚点未锁定时，在 Microsoft Word 中移动形状也可以移动 形状锚点。

## 例子

演示如何锁定或解锁形状的段落锚点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// 将“AnchorLocked”属性设置为“true”以防止形状锚定
// 在 Microsoft Word 中移动形状时避免移动。
// 将“AnchorLocked”属性设置为“false”以允许形状的任何移动
// 将其锚点移动到形状最终接近的任何其他段落。
shape.AnchorLocked = anchorLocked;

// 如果形状的左侧没有可见的锚符号，
// 我们需要通过“选项”启用可见锚点 -> 「显示」-> “对象锚”。
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
