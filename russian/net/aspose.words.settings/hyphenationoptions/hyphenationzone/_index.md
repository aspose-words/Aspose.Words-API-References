---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: Aspose.Words для .NET
description: Оптимизируйте макет текста с помощью свойства HyphenationZone. Управляйте расстоянием переноса от правого поля для более чистых, профессиональных документов.
type: docs
weight: 50
url: /ru/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Возвращает или задает расстояние в 1/20 пункта от правого поля, в пределах которого не требуется переносить слова. Значение по умолчанию для этого свойства — 360 (0,25 дюйма).

```csharp
public int HyphenationZone { get; set; }
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
