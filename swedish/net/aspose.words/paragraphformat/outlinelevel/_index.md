---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words för .NET
description: ParagraphFormat OutlineLevel fast egendom. Anger konturnivån för stycket i dokumentet i C#.
type: docs
weight: 250
url: /sv/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Anger konturnivån för stycket i dokumentet.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Exempel

Visar hur du konfigurerar styckekonturnivåer för att skapa hopfällbar text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke har en OutlineLevel, som kan vara valfritt tal från 1 till 9, eller med standardvärdet "BodyText".
// Om du ställer in egenskapen till ett av de numrerade värdena visas en pil till vänster
// i början av stycket.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Nivå 1 är den översta nivån. Om det finns ett stycke med en lägre nivå under ett stycke med en högre nivå,
// att komprimera stycket på högre nivå kommer att komprimera stycket på lägre nivå.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Två stycken på samma nivå kommer inte att kollapsa varandra,
// och pilarna kollapsar inte styckena de pekar på.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Standardvärdet för "BodyText" är det lägsta, vilket ett stycke på vilken nivå som helst kan kollapsa.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Se även

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
