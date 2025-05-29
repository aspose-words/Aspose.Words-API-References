---
title: BarcodeParameters.PosCodeStyle
linktitle: PosCodeStyle
articleTitle: PosCodeStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BarcodeParameters PosCodeStyle для штрихкодов точек продаж. Поддерживает UPCA, EAN13 и другие. Улучшите свою систему POS сегодня!
type: docs
weight: 140
url: /ru/net/aspose.words.fields/barcodeparameters/poscodestyle/
---
## BarcodeParameters.PosCodeStyle property

Стиль штрихкода точки продажи (типы штрихкодов UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Допустимые значения (без учета регистра): [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

## Примеры

Показывает, как использовать генератор штрихкодов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Мы можем использовать пользовательскую реализацию IBarcodeGenerator для генерации штрихкодов,
// а затем вставить их в документ как изображения.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Ниже приведены четыре примера различных типов штрихкодов, которые мы можем создать с помощью нашего генератора.
// Для каждого штрихкода мы указываем новый набор параметров штрихкода, а затем генерируем изображение.
// После этого мы можем вставить изображение в документ или сохранить его в локальной файловой системе.
// 1 - QR-код:
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

// 2 - штрих-код EAN13:
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

// 3 - штрих-код CODE39:
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

// 4 - штрих-код ITF14:
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

### Смотрите также

* class [BarcodeParameters](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
