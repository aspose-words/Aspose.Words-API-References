---
title: Watermarker.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: 使用我们的创新方法创建一个新的水印处理器，轻松增强您的图像并保护您的内容。
type: docs
weight: 10
url: /zh/net/aspose.words.lowcode/watermarker/create/
---
## Watermarker.Create method

创建水印处理器的新实例。

```csharp
public static Watermarker Create(WatermarkerContext context)
```

## 例子

显示如何使用上下文将水印文本插入文档。

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

显示如何使用上下文将水印图像插入到文档中。

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

展示如何使用上下文从流中将水印文本插入到文档中。

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

展示如何使用上下文从流中将水印图像插入到文档中。

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### 也可以看看

* class [WatermarkerContext](../../watermarkercontext/)
* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
