---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words для .NET
description: Оптимизируйте изображения PDF с помощью свойства JpegQuality в PdfSaveOptions, позволяющего контролировать качество JPEG для получения потрясающих визуальных эффектов в документах.
type: docs
weight: 220
url: /ru/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Возвращает или задает значение, определяющее качество изображений JPEG в документе PDF.

```csharp
public int JpegQuality { get; set; }
```

## Примечания

Значение по умолчанию — 100.

Это свойство используется совместно с[`ImageCompression`](../imagecompression/) вариант.

Действует только в том случае, если документ содержит изображения JPEG.

Используйте это свойство для получения или установки качества изображений внутри документа при сохранении в формате PDF. Значение может варьироваться от 0 до 100, где 0 означает наихудшее качество, но максимальное сжатие, а 100 означает наилучшее качество, но минимальное сжатие. Если качество равно 100, а исходное изображение — JPEG, это означает отсутствие сжатия — исходные байты будут сохранены.

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

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
