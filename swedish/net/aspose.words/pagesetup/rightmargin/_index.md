---
title: PageSetup.RightMargin
linktitle: RightMargin
articleTitle: RightMargin
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup RightMargin, justera enkelt högermarginalen i punkter för optimal textlayout och förbättrad dokumentpresentation.
type: docs
weight: 370
url: /sv/net/aspose.words/pagesetup/rightmargin/
---
## PageSetup.RightMargin property

Returnerar eller anger avståndet (i punkter) mellan sidans högra kant och brödtextens högra kant.

```csharp
public double RightMargin { get; set; }
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
