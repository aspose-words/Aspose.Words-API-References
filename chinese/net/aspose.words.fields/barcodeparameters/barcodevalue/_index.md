---
title: BarcodeParameters.BarcodeValue
linktitle: BarcodeValue
articleTitle: BarcodeValue
second_title: 用于 .NET 的 Aspose.Words
description: BarcodeParameters BarcodeValue 财产. 要编码的数据 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.fields/barcodeparameters/barcodevalue/
---
## BarcodeParameters.BarcodeValue property

要编码的数据。

```csharp
public string BarcodeValue { get; set; }
```

## 例子

展示如何使用条形码生成器。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以使用自定义的 IBarcodeGenerator 实现来生成条形码，
// 然后将它们作为图像插入到文档中。
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// 下面是我们可以使用生成器创建的不同条形码类型的四个示例。
// 对于每个条码，我们指定一组新的条码参数，然后生成图像。
// 之后，我们可以将图片插入到文档中，或者保存到本地文件系统中。
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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");

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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
builder.InsertImage(img);

// 3 - CODE39 条形码：
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - ITF14 条形码：
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "ITF14",
    BarcodeValue = "09312345678907",
    CaseCodeStyle = "STD"
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.ITF14.jpg");
builder.InsertImage(img);

doc.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.docx");
```

### 也可以看看

* class [BarcodeParameters](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
