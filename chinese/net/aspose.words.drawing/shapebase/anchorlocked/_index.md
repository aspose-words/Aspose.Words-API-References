---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words for .NET
description: 探索 ShapeBase AnchorLocked 属性来控制形状的锚锁定，增强项目的设计稳定性和灵活性。
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

仅对顶层形状有效。

此属性会影响 Microsoft Word 中形状锚点的行为。 当锚点未锁定时，在 Microsoft Word 中移动形状也会移动 形状的锚点。

## 例子

展示如何锁定或解锁形状的段落锚点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// 将“AnchorLocked”属性设置为“true”以防止形状的锚点
// 在 Microsoft Word 中移动形状时移动。
// 将“AnchorLocked”属性设置为“false”以允许形状的任何移动
// 还将其锚点移动到形状最终靠近的任何其他段落。
shape.AnchorLocked = anchorLocked;

// 如果形状左侧没有可见的锚符号，
// 我们需要通过“选项”->“显示”->“对象锚点”启用可见锚点。
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
