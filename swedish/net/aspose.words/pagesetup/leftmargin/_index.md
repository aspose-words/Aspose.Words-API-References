---
title: PageSetup.LeftMargin
linktitle: LeftMargin
articleTitle: LeftMargin
second_title: Aspose.Words för .NET
description: PageSetup LeftMargin fast egendom. Returnerar eller ställer in avståndet i poäng mellan sidans vänstra kant och brödtextens vänstra kant i C#.
type: docs
weight: 200
url: /sv/net/aspose.words/pagesetup/leftmargin/
---
## PageSetup.LeftMargin property

Returnerar eller ställer in avståndet (i poäng) mellan sidans vänstra kant och brödtextens vänstra kant.

```csharp
public double LeftMargin { get; set; }
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
