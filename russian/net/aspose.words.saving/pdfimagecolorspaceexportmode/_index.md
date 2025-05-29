---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words PdfImageColorSpaceExportMode, позволяющее оптимизировать выбор цвета изображения в документах PDF для получения потрясающих визуальных эффектов.
type: docs
weight: 6270
url: /ru/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Указывает, как будет выбрано цветовое пространство для изображений в документе PDF.

```csharp
public enum PdfImageColorSpaceExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Aspose.Words автоматически выбирает наиболее подходящее цветовое пространство для каждого изображения. |
| SimpleCmyk | `1` | Aspose.Words преобразует изображения RGB в цветовое пространство CMYK, используя простую формулу. |

## Примеры

Показывает, как установить другое цветовое пространство для изображений в документе при экспорте его в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Установите свойство "ImageColorSpaceExportMode" на "PdfImageColorSpaceExportMode.Auto", чтобы Aspose.Words
// автоматически выбирает цветовое пространство для изображений в документе, который преобразуется в PDF.
// В большинстве случаев цветовое пространство будет RGB.
// Установите свойство "ImageColorSpaceExportMode" на "PdfImageColorSpaceExportMode.SimpleCmyk"
// для использования цветового пространства CMYK для всех изображений в сохраненном PDF-файле.
// Aspose.Words также применит сжатие Flate ко всем изображениям и проигнорирует значение свойства «ImageCompression».
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
