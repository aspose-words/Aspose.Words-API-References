---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство кодировки HtmlFixedSaveOptions для бесшовного экспорта HTML. Легко установите кодировку UTF-8 с BOM для оптимальной целостности данных.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Указывает кодировку, используемую при экспорте в HTML. Значение по умолчанию:`новая кодировка UTF8(истина)` (UTF-8 с BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Примеры

Показывает, как выбрать кодировку, используемую при экспорте документа в HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Кодировка по умолчанию — UTF-8. Если мы хотим представить наш документ с использованием другой кодировки,
// мы можем использовать объект SaveOptions для установки определенной кодировки.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
