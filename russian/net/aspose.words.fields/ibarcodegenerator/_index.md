---
title: IBarcodeGenerator Interface
linktitle: IBarcodeGenerator
articleTitle: IBarcodeGenerator
second_title: Aspose.Words для .NET
description: Aspose.Words.Fields.IBarcodeGenerator интерфейс. Открытый интерфейс для пользовательского генератора штрихкодов. Реализация должна быть предоставлена пользователем на С#.
type: docs
weight: 2660
url: /ru/net/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface

Открытый интерфейс для пользовательского генератора штрих-кодов. Реализация должна быть предоставлена пользователем.

```csharp
public interface IBarcodeGenerator
```

## Методы

| Имя | Описание |
| --- | --- |
| [GetBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getbarcodeimage/)(*[BarcodeParameters](../barcodeparameters/)*) | Создать изображение штрих-кода, используя набор параметров (для поля DisplayBarcode). |
| [GetOldBarcodeImage](../../aspose.words.fields/ibarcodegenerator/getoldbarcodeimage/)(*[BarcodeParameters](../barcodeparameters/)*) | Создать изображение штрих-кода, используя набор параметров (для поля «старомодный штрих-код»). |

## Примечания

Экземпляр генератора должен быть передан через[`BarcodeGenerator`](../fieldoptions/barcodegenerator/) свойство.

## Примеры

Показывает, как использовать генератор штрих-кода.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Мы можем использовать собственную реализацию IBarcodeGenerator для генерации штрих-кодов,
// а затем вставляем их в документ как изображения.
doc.FieldOptions.BarcodeGenerator = new CustomBarcodeGenerator();

// Ниже приведены четыре примера различных типов штрих-кодов, которые мы можем создать с помощью нашего генератора.
// Для каждого штрих-кода мы указываем новый набор параметров штрих-кода, а затем генерируем изображение.
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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.QR.jpg");

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
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.EAN13.jpg");
builder.InsertImage(img);

// 3 - штрих-код CODE39:
barcodeParameters = new BarcodeParameters
{
    BarcodeType = "CODE39",
    BarcodeValue = "12345ABCDE",
    AddStartStopChar = true
};

img = doc.FieldOptions.BarcodeGenerator.GetBarcodeImage(barcodeParameters);
img.Save(ArtifactsDir + "FieldOptions.BarcodeGenerator.CODE39.jpg");
builder.InsertImage(img);

// 4 - штрих-код ITF14:
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

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
