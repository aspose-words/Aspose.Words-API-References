---
title: ParagraphFormat.SpaceBeforeAuto
linktitle: SpaceBeforeAuto
articleTitle: SpaceBeforeAuto
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat SpaceBeforeAuto. Justera automatiskt styckeavståndet för ett elegant och professionellt utseende i dina dokument.
type: docs
weight: 340
url: /sv/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

Sant om avståndet före stycket ställs in automatiskt.

```csharp
public bool SpaceBeforeAuto { get; set; }
```

## Anmärkningar

När den är inställd på`sann` , åsidosätter effekten av[`SpaceBefore`](../spacebefore/).

När du ställer in styckeavstånd före och styckeavstånd efter till Auto, lägger Microsoft Word automatiskt till 14 punkters avstånd mellan stycken enligt följande regler:

* Normalt läggs mellanrum till efter alla stycken.
* I en punktlista eller numrerad lista läggs avstånd endast till efter det sista objektet i listan. Avstånd läggs inte till mellan listobjekten.
* en kapslad punktlista eller numrerad lista läggs inget avstånd till.
* Mellanrum läggs normalt till efter en tabell.
* Mellanrum läggs inte till efter en tabell om det är det sista blocket i en tabellcell.
* Mellanrum läggs inte till efter det sista stycket i en tabellcell.

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

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
