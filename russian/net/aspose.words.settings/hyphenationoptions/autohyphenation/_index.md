---
title: HyphenationOptions.AutoHyphenation
linktitle: AutoHyphenation
articleTitle: AutoHyphenation
second_title: Aspose.Words для .NET
description: HyphenationOptions AutoHyphenation свойство. Получает или задает значение определяющее включена ли автоматическая расстановка переносов для документа. Значение по умолчанию для этого свойстваЛОЖЬ  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Получает или задает значение, определяющее, включена ли автоматическая расстановка переносов для документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` .

```csharp
public bool AutoHyphenation { get; set; }
```

## Примеры

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

* class [HyphenationOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
