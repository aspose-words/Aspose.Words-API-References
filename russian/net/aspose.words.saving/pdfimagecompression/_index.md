---
title: PdfImageCompression Enum
linktitle: PdfImageCompression
articleTitle: PdfImageCompression
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PdfImageCompression, которое оптимизирует сжатие изображений в ваших PDF-файлах, повышая качество и легко уменьшая размер файла.
type: docs
weight: 6280
url: /ru/net/aspose.words.saving/pdfimagecompression/
---
## PdfImageCompression enumeration

Указывает тип сжатия, применяемый к изображениям в файле PDF.

```csharp
public enum PdfImageCompression
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Автоматически выбирает наиболее подходящий тип сжатия для каждого изображения. |
| Jpeg | `1` | Сжатие JPEG. Не поддерживает прозрачность. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
