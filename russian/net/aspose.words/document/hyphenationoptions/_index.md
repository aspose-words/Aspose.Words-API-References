---
title: Document.HyphenationOptions
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Предоставляет доступ к параметрам расстановки переносов в документе.
type: docs
weight: 210
url: /ru/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Предоставляет доступ к параметрам расстановки переносов в документе.

```csharp
public HyphenationOptions HyphenationOptions { get; }
```

### Примеры

Показывает, как настроить автоматическую расстановку переносов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Смотрите также

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


