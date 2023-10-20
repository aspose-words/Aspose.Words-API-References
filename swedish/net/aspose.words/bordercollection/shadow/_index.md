---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words för .NET
description: BorderCollection Shadow fast egendom. Hämtar eller ställer in ett värde som anger om gränsen har en skugga i C#.
type: docs
weight: 110
url: /sv/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Hämtar eller ställer in ett värde som anger om gränsen har en skugga.

```csharp
public bool Shadow { get; set; }
```

## Anmärkningar

Får värdet från den första kanten i samlingen.

Ställer in värdet för alla kanter i samlingen exklusive diagonala kanter.

## Exempel

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

* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
