---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: Aspose.Words för .NET
description: ParagraphFormat RightIndent fast egendom. Hämtar eller ställer in värdet i poäng som representerar höger indrag för stycke i C#.
type: docs
weight: 270
url: /sv/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Hämtar eller ställer in värdet (i poäng) som representerar höger indrag för stycke.

```csharp
public double RightIndent { get; set; }
```

## Exempel

Visar hur du konfigurerar styckeformatering för att skapa text utanför centrum.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Centrera all text som dokumentbyggaren skriver och ställ in indrag.
// Indragskonfigurationen nedan kommer att skapa en text som kommer att sitta asymmetriskt på sidan.
// Mitten som vi justerar texten till kommer att vara mitten av texten, inte mitten av sidan.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
