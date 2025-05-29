---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words for .NET
description: 探索 ShapeBase BehindText 属性来控制设计中的形状分层，轻松增强文本可见性和布局精度。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

指定形状位于文本下方还是上方。

```csharp
public bool BehindText { get; set; }
```

## 评论

仅对顶层形状有效。

默认值为`错误的`。

## 例子

展示如何将浮动图像插入到页面的中心。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个浮动图像，该图像将出现在重叠文本后面，并将其与页面的中心对齐。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
