---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. När santSpaceBefore ochSpaceAfter kommer att ignoreras mellan styckena i samma stil.
type: docs
weight: 230
url: /sv/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

När sant,[`SpaceBefore`](../spacebefore/) och[`SpaceAfter`](../spaceafter/) kommer att ignoreras mellan styckena i samma stil.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

### Anmärkningar

Den här inställningen påverkar endast när den tillämpas på ett styckeformat. Om det tillämpas på ett stycke direkt, har det ingen effekt.

### Exempel

Visar hur man inte använder mellanrum mellan stycken med samma stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en stor mängd mellanrum före och efter stycken som den här byggaren kommer att skapa.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Ställ in "NoSpaceBetweenParagraphsOfSameStyle"-flaggan till "true" för att tillämpa
// inget mellanrum mellan stycken med samma stil, vilket kommer att gruppera liknande stycken.
// Lämna flaggan "NoSpaceBetweenParagraphsOfSameStyle" som "false"
// för att jämnt tillämpa mellanrum på varje stycke.
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
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


