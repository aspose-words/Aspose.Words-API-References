---
title: PageSetup.FooterDistance
linktitle: FooterDistance
second_title: Aspose.Words for .NET API Reference
description: PageSetup FooterDistance property. Returns or sets the distance in points between the footer and the bottom of the page in C#.
type: docs
weight: 140
url: /net/aspose.words/pagesetup/footerdistance/
---
## PageSetup.FooterDistance property

Returns or sets the distance (in points) between the footer and the bottom of the page.

```csharp
public double FooterDistance { get; set; }
```

## Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

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

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
