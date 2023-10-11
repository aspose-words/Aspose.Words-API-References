---
title: HtmlFixedSaveOptions.Encoding
second_title: Справочник по API Aspose.Words для .NET
description: HtmlFixedSaveOptions свойство. Указывает кодировку которая будет использоваться при экспорте в HTML. Значение по умолчаниюновая кодировка UTF8истина UTF8 со спецификацией.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Указывает кодировку, которая будет использоваться при экспорте в HTML. Значение по умолчанию:`новая кодировка UTF8(истина)` (UTF-8 со спецификацией).

```csharp
public Encoding Encoding { get; set; }
```

### Примеры

Показывает, как установить кодировку, которую следует использовать при экспорте документа в HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// Кодировка по умолчанию — UTF-8. Если мы хотим представить наш документ, используя другую кодировку,
// мы можем использовать объект SaveOptions для установки определенной кодировки.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* сборка [Aspose.Words](../../../)


