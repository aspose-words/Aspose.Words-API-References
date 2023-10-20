---
title: PageSetup.HeaderDistance
linktitle: HeaderDistance
articleTitle: HeaderDistance
second_title: Aspose.Words för .NET
description: PageSetup HeaderDistance fast egendom. Returnerar eller ställer in avståndet i poäng mellan sidhuvudet och toppen av sidan i C#.
type: docs
weight: 170
url: /sv/net/aspose.words/pagesetup/headerdistance/
---
## PageSetup.HeaderDistance property

Returnerar eller ställer in avståndet (i poäng) mellan sidhuvudet och toppen av sidan.

```csharp
public double HeaderDistance { get; set; }
```

## Exempel

Visar hur du justerar pappersstorlek, orientering, marginaler, tillsammans med andra inställningar för ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
