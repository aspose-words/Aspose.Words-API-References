---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BorderCollection Shadow för att förbättra dina designer. Kontrollera enkelt kantskuggor för ett modernt och elegant utseende i dina projekt!
type: docs
weight: 110
url: /sv/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Hämtar eller anger ett värde som anger om kanten har en skugga.

```csharp
public bool Shadow { get; set; }
```

## Anmärkningar

Hämtar värdet från den första kantlinjen i samlingen.

Anger värdet för alla ramar i samlingen exklusive diagonala ramar.

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
