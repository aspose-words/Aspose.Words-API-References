---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words for .NET
description: 发现 PageSetup PageWidth 属性可以轻松调整页面宽度（以点为单位），增强文档布局以实现最佳显示效果。
type: docs
weight: 340
url: /zh/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

返回或设置页面宽度（以磅为单位）。

```csharp
public double PageWidth { get; set; }
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

展示如何插入浮动图像，并指定其位置和大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// 配置形状的“RelativeHorizontalPosition”属性来处理“Left”属性的值
// 作为形状与页面左侧的水平距离（以点为单位）。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// 将形状与页面左侧的水平距离设置为 100。
shape.Left = 100;

// 以类似的方式使用“RelativeVerticalPosition”属性将形状定位在页面顶部下方 80pt 处。
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// 设置形状的高度，它将自动缩放宽度以保留尺寸。
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// “Bottom”和“Right”属性包含图像的底部和右侧边缘。
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
