---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BorderCollection DistanceFromText för att enkelt anpassa kantavståndet från texten i dina designer. Optimera din layout utan ansträngning!
type: docs
weight: 40
url: /sv/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Hämtar eller ställer in avståndet mellan kantlinjen och texten i punkter.

```csharp
public double DistanceFromText { get; set; }
```

## Anmärkningar

Hämtar avståndet från texten för den första ramen.

Anger avståndet från texten för alla ramar i samlingen exklusive diagonala ramar.

Har ingen effekt och kommer automatiskt att nollställas för kantlinjer runt tabellceller.

## Exempel

Visar hur man skapar en grön vågig sidkantlinje med en skugga.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Se även

* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
