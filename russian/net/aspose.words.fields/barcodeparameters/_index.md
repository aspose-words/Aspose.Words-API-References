---
title: BarcodeParameters Class
linktitle: BarcodeParameters
articleTitle: BarcodeParameters
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.BarcodeParameters — ваш основной инструмент для бесперебойной генерации и настройки штрихкодов при обработке документов.
type: docs
weight: 1880
url: /ru/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Класс-контейнер для параметров штрих-кода, передаваемых в BarcodeGenerator.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class BarcodeParameters
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [BarcodeParameters](barcodeparameters/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/barcodeparameters/addstartstopchar/) { get; set; } | Добавлять ли символы Start/Stop для типов штрих-кодов NW7 и CODE39. |
| [BackgroundColor](../../aspose.words.fields/barcodeparameters/backgroundcolor/) { get; set; } | Цвет фона штрих-кода (0x000000 - 0xFFFFFF) |
| [BarcodeType](../../aspose.words.fields/barcodeparameters/barcodetype/) { get; set; } | Тип штрих-кода. |
| [BarcodeValue](../../aspose.words.fields/barcodeparameters/barcodevalue/) { get; set; } | Данные для кодирования. |
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Стиль кода корпуса для типа штрих-кода ITF14. Допустимые значения: [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Отображать ли данные штрих-кода (текст) вместе с изображением. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Уровень исправления ошибок QR-кода. Допустимые значения: [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Тип лицевого опознавательного знака (ЛИМ). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | Исправлять ли контрольную цифру, если она недействительна. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Цвет переднего плана штрих-кода (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Будь то[`PostalAddress`](./postaladdress/) это имя закладки. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Будь то[`PostalAddress`](./postaladdress/) почтовый адрес в США. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Стиль штрихкода точки продажи (типы штрихкодов UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Допустимые значения (без учета регистра): [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Штрих-код почтового адреса. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Коэффициент масштабирования для символа. Значение указывается в целых процентных пунктах, допустимые значения: [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Высота изображения штрих-кода (в твипах - 1/1440 дюйма) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Вращение символа штрих-кода. Допустимые значения: [0, 3]. |

## Примечания

Набор параметров соответствует параметрам поля DISPLAYBARCODE. Точный список см. на странице[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
