---
title: PageSetup.Borders
second_title: Aspose.Words för .NET API Referens
description: PageSetup fast egendom. Hämtar en samling av sidkanterna.
type: docs
weight: 50
url: /sv/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Hämtar en samling av sidkanterna.

```csharp
public BorderCollection Borders { get; }
```

### Exempel

Visar hur man skapar grön vågig sidkant med en skugga.

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../pagesetup/)
* hopsättning [Aspose.Words](../../../)


