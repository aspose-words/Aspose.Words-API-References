---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Drawing.WrapType 枚举如何增强文本环绕形状和图像以实现专业的文档格式。
type: docs
weight: 1810
url: /zh/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

指定文本如何环绕形状或图片。

```csharp
public enum WrapType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `3` | 形状周围没有文字环绕。形状位于文字后面或前面。 |
| Inline | `0` | 形状与文本保留在同一层，并被视为字符。 |
| TopBottom | `1` | 文本在形状顶部停止，并在形状下方的行重新开始。 |
| Square | `2` | 将文本环绕在形状方形边界框的所有边上。 |
| Tight | `4` | 紧紧包裹形状的边缘，而不是包裹边界框。 |
| Through | `5` | 与紧密相同，但包裹形状中任何开放的部分。 |

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

展示如何插入图像并将其用作水印。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将图像插入页眉，以便它在每个页面上都可见。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// 将图像放置在页面的中心。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### 也可以看看

* property [WrapType](../shapebase/wraptype/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
