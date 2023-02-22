---
title: ParagraphFormat.RightIndent
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar eller ställer in värdet i poäng som representerar höger indrag för stycke.
type: docs
weight: 260
url: /sv/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Hämtar eller ställer in värdet (i poäng) som representerar höger indrag för stycke.

```csharp
public double RightIndent { get; set; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


