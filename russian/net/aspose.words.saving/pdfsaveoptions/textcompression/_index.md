---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words для .NET
description: PdfSaveOptions TextCompression свойство. Указывает тип сжатия который будет использоваться для всего текстового содержимого в документе на С#.
type: docs
weight: 290
url: /ru/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Указывает тип сжатия, который будет использоваться для всего текстового содержимого в документе.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Примечания

По умолчаниюFlate.

Значительно увеличивает размер вывода при сохранении документа без сжатия.

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

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
