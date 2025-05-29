---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions ImageColorSpaceExportMode, позволяющее оптимизировать выбор цвета изображения в ваших PDF-файлах для достижения потрясающего визуального качества и согласованности.
type: docs
weight: 190
url: /ru/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

Указывает, как будет выбрано цветовое пространство для изображений в документе PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## Примечания

Значение по умолчанию:Auto .

ЕслиSimpleCmyk значение указано, [`ImageCompression`](../imagecompression/) опция игнорируется и Для всех изображений в документе используется сжатие Flate.

SimpleCmyk значение не поддерживается при сохранении в PDF/A. Auto Вместо этого будет использовано значение .

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

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
