---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.PdfTextCompression перечисление. Указывает тип сжатия применяемый ко всему содержимому PDFфайла кроме изображений на С#.
type: docs
weight: 5530
url: /ru/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Указывает тип сжатия, применяемый ко всему содержимому PDF-файла, кроме изображений.

```csharp
public enum PdfTextCompression
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Без сжатия. |
| Flate | `1` | Плоское (ZIP) сжатие. |

## Примеры

Показывает, как применить сжатие текста при сохранении документа в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства TextCompression значение «PdfTextCompression.None», чтобы не применять какие-либо
// сжатие в текст при сохранении документа в PDF.
// Установите для свойства TextCompression значение «PdfTextCompression.Flate», чтобы применить сжатие ZIP.
// в текст, когда мы сохраняем документ в PDF. Чем больше документ, тем большее влияние он окажет.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
