---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ConsecutiveHyphenLimit в HyphenationOptions. Контролируйте использование дефисов в тексте для улучшения читаемости и форматирования. По умолчанию 0.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Возвращает или задает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства — 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## Примечания

Если значение этого свойства равно 0, любое количество последовательных строк может заканчиваться дефисами.

Свойство не действует при сохранении в форматах с фиксированным размером страницы, например, PDF.

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
