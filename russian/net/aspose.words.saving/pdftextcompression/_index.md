---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PdfTextCompression для эффективного сжатия содержимого PDF-файлов, увеличения размера файла и производительности при сохранении качества.
type: docs
weight: 6330
url: /ru/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Указывает тип сжатия, применяемый ко всему содержимому PDF-файла, за исключением изображений.

```csharp
public enum PdfTextCompression
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Без сжатия. |
| Flate | `1` | Сжатие Flate (ZIP). |

## Примеры

Показывает, как применять сжатие текста при сохранении документа в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "TextCompression" на "PdfTextCompression.None", чтобы не применять никаких
// сжатие в текст при сохранении документа в формате PDF.
// Установите свойство "TextCompression" на "PdfTextCompression.Flate", чтобы применить сжатие ZIP
// в текст при сохранении документа в PDF. Чем больше документ, тем больше будет влияние.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
