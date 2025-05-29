---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font TextEffect för att enkelt anpassa teckensnittsanimationer och förbättra dina designer med dynamiska texteffekter för en fängslande användarupplevelse.
type: docs
weight: 460
url: /sv/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Hämtar eller ställer in teckensnittsanimationseffekten.

```csharp
public TextEffect TextEffect { get; set; }
```

## Exempel

Visar hur man tillämpar en visuell effekt på en löprunda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Äldre versioner av Microsoft Word stöder endast teckensnittsanimationseffekter.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Se även

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
