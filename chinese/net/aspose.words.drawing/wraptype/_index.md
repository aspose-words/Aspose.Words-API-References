---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.WrapType 枚举. 指定文本如何环绕形状或图片 在 C#.
type: docs
weight: 1400
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
| None | `3` | 形状周围没有文字。形状放置在文本的后面或前面。 |
| Inline | `0` | 形状与文本保持在同一图层上并被视为字符。 |
| TopBottom | `1` | 文本在形状顶部停止并在形状下方的行重新开始。 |
| Square | `2` | 将文本环绕在形状的方形边界框的所有边上。 |
| Tight | `4` | 紧紧围绕形状的边缘，而不是围绕边界框。 |
| Through | `5` | 与 Tight 相同，但包裹在任何打开的形状部分内。 |

## 例子

演示如何将浮动图像插入页面中心。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入将出现在重叠文本后面的浮动图像，并将其与页面中心对齐。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

演示如何插入图像并将其用作水印。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将图像插入到页眉中，以便在每个页面上都可见。
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// 将图片放在页面的中心。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

演示如何插入图像并将其用作水印 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将图像插入到页眉中，以便在每个页面上都可见。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // 将图片放在页面的中心。
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### 也可以看看

* property [WrapType](../shapebase/wraptype/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
