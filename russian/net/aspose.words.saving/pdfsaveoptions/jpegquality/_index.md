---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words для .NET
description: PdfSaveOptions JpegQuality свойство. Получает или задает значение определяющее качество изображений JPEG в документе PDF на С#.
type: docs
weight: 220
url: /ru/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Получает или задает значение, определяющее качество изображений JPEG в документе PDF.

```csharp
public int JpegQuality { get; set; }
```

## Примечания

Значение по умолчанию — 100.

Это свойство используется совместно с[`ImageCompression`](../imagecompression/) вариант.

Действует только в том случае, если документ содержит изображения JPEG.

Используйте это свойство, чтобы получить или установить качество изображений внутри документа при сохранении в формате PDF. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 означает лучшее качество, но минимальное сжатие. Если качество равно 100, а исходное изображение — JPEG, это означает отсутствие сжатия — исходные байты будут сохранены.

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

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Установите для свойства ImageCompression значение «PdfImageCompression.Auto», чтобы использовать
// Свойство «ImageCompression» для управления качеством изображений Jpeg, которые попадают в выходной PDF-файл.
// Установите для свойства «ImageCompression» значение «PdfImageCompression.Jpeg», чтобы использовать
// Свойство «ImageCompression» для управления качеством всех изображений, попадающих в выходной PDF-файл.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Установите для свойства «JpegQuality» значение «10», чтобы усилить сжатие за счет качества изображения.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
