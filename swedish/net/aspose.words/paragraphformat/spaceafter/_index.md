---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words för .NET
description: Styr styckeavståndet med egenskapen SpaceAfter. Justera enkelt avståndet i punkter för att förbättra dokumentets läsbarhet och presentation.
type: docs
weight: 310
url: /sv/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

Hämtar eller anger avståndet (i punkter) efter stycket.

```csharp
public double SpaceAfter { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta ett värde när argumentet låg utanför intervallet för giltiga värden. |

## Anmärkningar

Har ingen effekt när[`SpaceAfterAuto`](../spaceafterauto/) är`sann`.

Giltiga värden sträcker sig från 0 till 1584.

## Exempel

Visar hur man ställer in automatiskt styckeavstånd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en stor mängd avstånd före och efter stycken som den här verktygsbyggaren kommer att skapa.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Sätt dessa flaggor till "true" för att tillämpa automatiskt avstånd,
// ignorerar effektivt avståndet i egenskaperna vi angav ovan.
// Om du lämnar dem som "falskt" tillämpas vårt anpassade styckeavstånd.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Infoga två stycken med mellanrum ovanför och nedanför och spara dokumentet.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Visar hur man använder avståndsfria stycken med samma stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en stor mängd avstånd före och efter stycken som den här verktygsbyggaren kommer att skapa.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Sätt flaggan "NoSpaceBetweenParagraphsOfSameStyle" till "true" för att tillämpa
// inget mellanrum mellan stycken med samma stil, vilket grupperar liknande stycken.
// Lämna flaggan "NoSpaceBetweenParagraphsOfSameStyle" som "false"
// för att tillämpa jämnt avstånd i varje stycke.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
