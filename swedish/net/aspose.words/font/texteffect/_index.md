---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words för .NET
description: Font TextEffect fast egendom. Får eller ställer in teckensnittsanimeringseffekten i C#.
type: docs
weight: 450
url: /sv/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Får eller ställer in teckensnittsanimeringseffekten.

```csharp
public TextEffect TextEffect { get; set; }
```

## Exempel

Visar hur man applicerar en visuell effekt på en löpning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Äldre versioner av Microsoft Word stöder endast teckensnittsanimeringseffekter.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Se även

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
