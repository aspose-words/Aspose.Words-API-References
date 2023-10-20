---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words för .NET
description: Font UnderlineColor fast egendom. Hämtar eller ställer in färgen på understrykningen som appliceras på teckensnittet i C#.
type: docs
weight: 540
url: /sv/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Hämtar eller ställer in färgen på understrykningen som appliceras på teckensnittet.

```csharp
public Color UnderlineColor { get; set; }
```

## Exempel

Visar hur du konfigurerar stilen och färgen på en textunderstrykning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
