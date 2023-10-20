---
title: PdfImageCompression Enum
linktitle: PdfImageCompression
articleTitle: PdfImageCompression
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.PdfImageCompression перечисление. Указывает тип сжатия применяемый к изображениям в файле PDF на С#.
type: docs
weight: 5490
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
| Auto | `0` | Автоматически выбирает наиболее подходящее сжатие для каждого изображения. |
| Jpeg | `1` | Сжатие Jpeg. Не поддерживает прозрачность. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
