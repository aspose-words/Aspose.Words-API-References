---
title: ParagraphFormat.SpaceBeforeAuto
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Sant om mängden avstånd före stycket ställs in automatiskt.
type: docs
weight: 330
url: /sv/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

Sant om mängden avstånd före stycket ställs in automatiskt.

```csharp
public bool SpaceBeforeAuto { get; set; }
```

### Anmärkningar

När inställd på`Sann` , åsidosätter effekten av[`SpaceBefore`](../spacebefore/).

När du ställer in styckemellanslag före och mellanslag efter till Auto, lägger Microsoft Word till 14 punkters avstånd mellan stycken automatiskt enligt följande regler:

* Normalt läggs mellanrum efter alla stycken.
* I en punktlista eller numrerad lista läggs avstånd endast till efter det sista objektet i listan. Avstånd läggs inte till mellan listobjekten.
* en kapslad punktlista eller numrerad lista läggs inte avstånd till.
* Mellanrum läggs normalt till efter en tabell.
* Mellanrum läggs inte till efter en tabell om det är det sista blocket i en tabellcell.
* Mellanrum läggs inte till efter det sista stycket i en tabellcell.

### Exempel

Visar hur man ställer in automatiskt styckeavstånd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en stor mängd mellanrum före och efter stycken som den här byggaren kommer att skapa.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Ställ in dessa flaggor på "true" för att tillämpa automatiskt mellanrum,
// ignorerar effektivt avståndet i egenskaperna vi ställt in ovan.
// Lämna dem som "false" kommer att tillämpa vårt anpassade styckeavstånd.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Infoga två stycken som kommer att ha mellanrum ovanför och under dem och spara dokumentet.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


