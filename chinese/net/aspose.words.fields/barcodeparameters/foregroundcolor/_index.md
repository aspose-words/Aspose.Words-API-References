---
title: BarcodeParameters.ForegroundColor
linktitle: ForegroundColor
articleTitle: ForegroundColor
second_title: Aspose.Words for .NET
description: 探索 BarcodeParameters 的 ForegroundColor 属性，自定义条形码颜色（范围从 0x000000 到 0xFFFFFF）。立即提升您的条形码设计！
type: docs
weight: 110
url: /zh/net/aspose.words.fields/barcodeparameters/foregroundcolor/
---
## BarcodeParameters.ForegroundColor property

条形码前景色 (0x000000 - 0xFFFFFF)

```csharp
public string ForegroundColor { get; set; }
```

## 例子

展示如何使用条形码生成器。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 我们可以使用自定义的 IBarcodeGenerator 实现来生成条形码，
// 然后将它们作为图像插入到文档中。
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// 下面是我们可以使用生成器创建的四种不同条形码类型的示例。
// 对于每个条形码，我们指定一组新的条形码参数，然后生成图像。
// 之后，我们可以将图像插入文档，或将其保存到本地文件系统。
// 1 - 二维码：
BarcodeParameters barcodeParameters = new BarcodeParameters
{
    BarcodeType = "QR",
    BarcodeValue = "ABC123",
    BackgroundColor = "0xF8BD69",
    ForegroundColor = "0xB5413B",
    ErrorCorrectionLevel = "3",
    ScalingFactor = "250",
    SymbolHeight = "1000",
    SymbolRotation = "0"
};

Image img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 2 - EAN13 条形码：
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "EAN13",
    BarcodeValue = "501234567890",
    DisplayText = true,
    PosCodeStyle = "CASE",
    FixCheckDigit = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 3 - CODE39 条形码：
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

// 4 - ITF14 条形码：
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
#if NET461_OR_GREATER || JAVA
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
#elif NET5_0_OR_GREATER
using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg"))
{
    img.Encode(fs, SKEncodedImageFormat.Jpeg, 100);
}
#endif
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### 也可以看看

* class [BarcodeParameters](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
