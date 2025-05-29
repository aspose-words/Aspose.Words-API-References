---
title: PageSetup.BottomMargin
linktitle: BottomMargin
articleTitle: BottomMargin
second_title: Aspose.Words för .NET
description: Justera dokumentets layout med egenskapen PageSetup BottomMargin, som definierar avståndet mellan sidans nederkant och brödtexten för optimal presentation.
type: docs
weight: 80
url: /sv/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Returnerar eller anger avståndet (i punkter) mellan sidans nederkant och brödtextens nedre gräns.

```csharp
public double BottomMargin { get; set; }
```

## Exempel

Visar hur man justerar pappersstorlek, orientering, marginaler och andra inställningar för ett avsnitt.

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
