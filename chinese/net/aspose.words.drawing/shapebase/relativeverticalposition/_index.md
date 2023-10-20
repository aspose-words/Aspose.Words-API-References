---
title: ShapeBase.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase RelativeVerticalPosition 财产. 指定相对于形状垂直定位的位置 在 C#.
type: docs
weight: 440
url: /zh/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

指定相对于形状垂直定位的位置。

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

## 评论

默认值为Paragraph。

仅对顶级浮动形状有效。

## 例子

演示如何将浮动图像插入到页面中央。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个浮动图像，该图像将出现在重叠文本后面并将其与页面中心对齐。
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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
