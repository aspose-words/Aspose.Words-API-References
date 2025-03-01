---
title: PageSetup.RightMargin
linktitle: RightMargin
articleTitle: RightMargin
second_title: Aspose.Words for .NET
description: Discover the PageSetup RightMargin property, easily adjust the right margin in points for optimal text layout and enhanced document presentation.
type: docs
weight: 370
url: /net/aspose.words/pagesetup/rightmargin/
---
## PageSetup.RightMargin property

Returns or sets the distance (in points) between the right edge of the page and the right boundary of the body text.

```csharp
public double RightMargin { get; set; }
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
