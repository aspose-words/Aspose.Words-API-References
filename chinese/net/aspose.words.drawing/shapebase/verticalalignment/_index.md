---
title: ShapeBase.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words for .NET
description: 探索 ShapeBase VerticalAlignment 属性以优化形状的垂直定位，从而增强设计精度和视觉吸引力。
type: docs
weight: 600
url: /zh/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

指定形状的垂直定位方式。

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

## 评论

默认值为None。

仅对顶层浮动形状有效。

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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
