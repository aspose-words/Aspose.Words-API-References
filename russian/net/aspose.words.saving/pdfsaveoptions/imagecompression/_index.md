---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words для .NET
description: Оптимизируйте свой PDF-файл с помощью свойства ImageCompression в PdfSaveOptions, позволяющего выбрать наилучший тип сжатия для получения ярких, высококачественных изображений.
type: docs
weight: 200
url: /ru/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Указывает тип сжатия, который будет использоваться для всех изображений в документе.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Примечания

По умолчаниюAuto.

С использованиемJpeg позволяет контролировать качество изображений в выходном документе с помощью[`JpegQuality`](../jpegquality/) свойство.

С использованиемJpeg обеспечивает самую высокую скорость преобразования по сравнению с производительностью других типов сжатия, , но в этом случае происходит сжатие JPEG с потерями.

С использованиемAuto позволяет контролировать качество JPEG в выходном документе через[`JpegQuality`](../jpegquality/)свойство, но для других форматов необработанные пиксельные данные извлекаются и сохраняются со сжатием Flate. Этот случай медленнее, чем преобразование в JPEG, но без потерь.

## Примеры

Показывает, как указать тип сжатия для всех изображений в документе, который мы конвертируем в PDF.

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
// Установите свойство "ImageCompression" на "PdfImageCompression.Auto", чтобы использовать
// Свойство «ImageCompression» для управления качеством изображений JPEG, которые попадают в выходной PDF-файл.
// Установите свойство "ImageCompression" на "PdfImageCompression.Jpeg", чтобы использовать
// Свойство «ImageCompression» для управления качеством всех изображений, которые попадают в выходной PDF-файл.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Установите свойство «JpegQuality» на «10», чтобы усилить сжатие за счет качества изображения.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Смотрите также

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
