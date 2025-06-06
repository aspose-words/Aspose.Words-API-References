---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HyphenateCaps в HyphenationOptions. Легко управляйте переносами для слов, написанных заглавными буквами — по умолчанию установлено значение true. Оптимизируйте свой текст сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Возвращает или задает значение, определяющее, переносятся ли слова, написанные заглавными буквами. Значение по умолчанию для этого свойства:`истинный` .

```csharp
public bool HyphenateCaps { get; set; }
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
