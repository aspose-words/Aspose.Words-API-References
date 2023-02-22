---
title: PdfSaveOptions.ImageCompression
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Указывает тип сжатия который будет использоваться для всех изображений в документе.
type: docs
weight: 170
url: /ru/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Указывает тип сжатия, который будет использоваться для всех изображений в документе.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

### Примечания

По умолчаниюAuto.

С использованиемJpeg позволяет контролировать качество изображений в выходном документе с помощью[`JpegQuality`](../jpegquality/) имущество.

С использованиемJpeg обеспечивает самую высокую скорость преобразования по сравнению с производительностью других типов сжатия, , но в этом случае имеет место сжатие JPEG с потерями.

С использованиемAuto позволяет контролировать качество Jpeg в выходном документе через[`JpegQuality`](../jpegquality/) свойство, , но для других форматов необработанные пиксельные данные извлекаются и сохраняются с помощью сжатия Flate. Этот случай медленнее, чем преобразование Jpeg, но без потерь.

### Примеры

Показывает, как указать тип сжатия для всех изображений в документе, который мы конвертируем в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Установите для свойства "ImageCompression" значение "PdfImageCompression.Auto", чтобы использовать
// Свойство «ImageCompression» для управления качеством изображений Jpeg, которые попадают в выходной PDF-файл.
// Установите для свойства "ImageCompression" значение "PdfImageCompression.Jpeg", чтобы использовать
// Свойство «ImageCompression» для управления качеством всех изображений, которые попадают в выходной PDF-файл.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Установите для свойства "JpegQuality" значение "10", чтобы усилить сжатие за счет снижения качества изображения.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Смотрите также

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


