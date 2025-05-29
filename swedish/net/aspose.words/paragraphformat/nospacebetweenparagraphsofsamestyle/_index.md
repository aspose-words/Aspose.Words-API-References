---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle. Optimera din dokumentlayout genom att eliminera mellanrum mellan stycken med samma stil.
type: docs
weight: 250
url: /sv/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

När`sann` ,[`SpaceBefore`](../spacebefore/) och[`SpaceAfter`](../spaceafter/) kommer att ignoreras mellan stycken med samma formatmall.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Anmärkningar

Den här inställningen gäller bara när den tillämpas på ett styckeformat. Om den tillämpas direkt på ett stycke har den ingen effekt.

## Exempel

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
