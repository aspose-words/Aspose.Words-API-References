---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Kantskugga för att förbättra din design! Kontrollera skuggeffekter för kanter och höj ditt användargränssnitt med fantastisk grafik.
type: docs
weight: 60
url: /sv/net/aspose.words/border/shadow/
---
## Border.Shadow property

Hämtar eller anger ett värde som anger om kanten har en skugga.

```csharp
public bool Shadow { get; set; }
```

## Anmärkningar

I Microsoft Word, för att en kantlinje ska ha en skugga, måste kantlinjerna på alla fyra sidor (vänster, övre, högra och nedre) vara av samma typ, bredd, färg och alla måste ha egenskapen Skugga inställd på`sann`.

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

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
