---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions TextCompression для оптимизации ваших документов. Выберите лучший тип сжатия для эффективного хранения текста и более быстрой загрузки.
type: docs
weight: 310
url: /ru/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Указывает тип сжатия, который будет использоваться для всего текстового содержимого документа.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Примечания

По умолчаниюFlate.

Значительно увеличивает размер выходного файла при сохранении документа без сжатия.

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

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
