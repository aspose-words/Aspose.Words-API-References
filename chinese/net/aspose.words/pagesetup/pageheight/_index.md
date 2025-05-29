---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words for .NET
description: 探索 PageSetup PageHeight 属性以有效地管理文档的高度（以点为单位），从而增强布局和演示效果。
type: docs
weight: 310
url: /zh/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

返回或设置页面高度（以点为单位）。

```csharp
public double PageHeight { get; set; }
```

## 例子

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

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
