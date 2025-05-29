---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.RelativeHorizontalPosition 枚举来定义文档中形状和文本框的精确水平定位。
type: docs
weight: 1580
url: /zh/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

指定形状或文本框的水平位置的相对位置。

```csharp
public enum RelativeHorizontalPosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Margin | `0` | 指定水平定位应相对于页边距。 |
| Page | `1` | 对象相对于页面左边缘定位。 |
| Column | `2` | 该对象相对于列的左侧定位。 |
| Character | `3` | 对象相对于段落左侧定位。 |
| LeftMargin | `4` | 指定水平定位应相对于页面左边距。 |
| RightMargin | `5` | 指定水平定位应相对于页面的右边距。 |
| InsideMargin | `6` | 指定水平定位应相对于 当前页的内边距（奇数页的左边距，偶数页的右边距）。 |
| OutsideMargin | `7` | 指定水平定位应相对于 当前页的外边距（奇数页的右边距，偶数页的左边距）。 |
| Default | `2` | 默认值为Column. |

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

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
