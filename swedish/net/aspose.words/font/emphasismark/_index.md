---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen Teckensnittsmarkering för att förbättra din textformatering. Lär dig att ställa in och anpassa betoningstecken för bättre läsbarhet.
type: docs
weight: 110
url: /sv/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Hämtar eller ställer in betoningstecknet som tillämpas på denna formatering.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## Exempel

Visar hur man lägger till ytterligare tecken som renderas ovanför/under tecknet.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Möjliga typer av betoningstecken:
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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
