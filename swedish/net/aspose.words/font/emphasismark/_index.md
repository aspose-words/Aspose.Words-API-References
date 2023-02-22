---
title: Font.EmphasisMark
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Hämtar eller ställer in betoningen som appliceras på denna formatering.
type: docs
weight: 110
url: /sv/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Hämtar eller ställer in betoningen som appliceras på denna formatering.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

### Exempel

Visar hur man lägger till ytterligare tecken renderat ovanför/under tecknet.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Möjliga typer av betoningsmärke:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Se även

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


