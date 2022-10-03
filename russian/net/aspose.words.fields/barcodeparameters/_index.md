---
title: BarcodeParameters
second_title: Справочник по API Aspose.Words для .NET
description: Классконтейнер для параметров штрихкода для передачи в BarcodeGenerator.
type: docs
weight: 1320
url: /ru/net/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class

Класс-контейнер для параметров штрих-кода для передачи в BarcodeGenerator.

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
| [CaseCodeStyle](../../aspose.words.fields/barcodeparameters/casecodestyle/) { get; set; } | Стиль кода случая для штрих-кода типа ITF14. Допустимые значения: [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](../../aspose.words.fields/barcodeparameters/displaytext/) { get; set; } | Отображать ли данные штрих-кода (текст) вместе с изображением. |
| [ErrorCorrectionLevel](../../aspose.words.fields/barcodeparameters/errorcorrectionlevel/) { get; set; } | Уровень исправления ошибок QR-кода. Допустимые значения: [0, 3]. |
| [FacingIdentificationMark](../../aspose.words.fields/barcodeparameters/facingidentificationmark/) { get; set; } | Тип маркировки лицевой стороны (FIM). |
| [FixCheckDigit](../../aspose.words.fields/barcodeparameters/fixcheckdigit/) { get; set; } | Нужно ли исправлять контрольную цифру, если она недействительна. |
| [ForegroundColor](../../aspose.words.fields/barcodeparameters/foregroundcolor/) { get; set; } | Основной цвет штрих-кода (0x000000 - 0xFFFFFF) |
| [IsBookmark](../../aspose.words.fields/barcodeparameters/isbookmark/) { get; set; } | Будь то[`PostalAddress`](./postaladdress/) имя закладки. |
| [IsUSPostalAddress](../../aspose.words.fields/barcodeparameters/isuspostaladdress/) { get; set; } | Будь то[`PostalAddress`](./postaladdress/) почтовый адрес в США. |
| [PosCodeStyle](../../aspose.words.fields/barcodeparameters/poscodestyle/) { get; set; } | Стиль штрих-кода торговой точки (типы штрих-кода UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Допустимые значения (без учета регистра): [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [PostalAddress](../../aspose.words.fields/barcodeparameters/postaladdress/) { get; set; } | Почтовый адрес со штрих-кодом. |
| [ScalingFactor](../../aspose.words.fields/barcodeparameters/scalingfactor/) { get; set; } | Коэффициент масштабирования символа. Значение указано в целых процентах, допустимые значения: [10, 1000]. |
| [SymbolHeight](../../aspose.words.fields/barcodeparameters/symbolheight/) { get; set; } | Высота изображения штрих-кода (в твипах - 1/1440 дюйма) |
| [SymbolRotation](../../aspose.words.fields/barcodeparameters/symbolrotation/) { get; set; } | Вращение символа штрих-кода. Допустимые значения: [0, 3]. |

### Примечания

Набор параметров соответствует параметрам поля DISPLAYBARCODE. Точный список см. на[https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx](https://msdn.microsoft.com/en-us/library/hh745901(v=office.12).aspx)

### Примеры

Показывает, как использовать генератор штрих-кода.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем использовать собственную реализацию IBarcodeGenerator для генерации штрих-кодов,
// и затем вставляем их в документ как изображения.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
