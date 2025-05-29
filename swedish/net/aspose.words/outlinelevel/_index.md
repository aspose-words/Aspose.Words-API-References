---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.OutlineLevel-enum för att enkelt hantera styckedispositionsnivåer i dina dokument för förbättrad organisation och tydlighet.
type: docs
weight: 5060
url: /sv/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Anger dispositionsnivån för ett stycke i dokumentet.

```csharp
public enum OutlineLevel
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Level1 | `0` | Stycket är på dispositionsnivå 1 (översta nivån). |
| Level2 | `1` | Stycket är på dispositionsnivå 2. |
| Level3 | `2` | Stycket är på dispositionsnivå 3. |
| Level4 | `3` | Stycket är på dispositionsnivå 4. |
| Level5 | `4` | Stycket är på dispositionsnivå 5. |
| Level6 | `5` | Stycket är på dispositionsnivå 6. |
| Level7 | `6` | Stycket är på dispositionsnivå 7. |
| Level8 | `7` | Stycket är på dispositionsnivå 8. |
| Level9 | `8` | Stycket är på dispositionsnivå 9. |
| BodyText | `9` | Stycket är på samma nivå som huvudtexten. |

## Exempel

Visar hur man konfigurerar styckedispositionsnivåer för att skapa hopfällbar text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke har en OutlineLevel, som kan vara valfritt tal från 1 till 9, eller standardvärdet "BodyText".
// Om egenskapen ställs in på ett av de numrerade värdena visas en pil till vänster
// i början av stycket.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Nivå 1 är den översta nivån. Om det finns ett stycke med en lägre nivå under ett stycke med en högre nivå,
// om du komprimerar stycket på högre nivå komprimeras stycket på lägre nivå.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Två stycken på samma nivå kommer inte att komprimeras,
// och pilarna komprimerar inte stycken de pekar på.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Standardvärdet för "BodyText" är det lägsta värdet som ett stycke på vilken nivå som helst kan komprimera.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
