---
title: PageSetup.BottomMargin
linktitle: BottomMargin
articleTitle: BottomMargin
second_title: Aspose.Words for .NET
description: Adjust your document's layout with the PageSetup BottomMargin property, defining the space between the page's bottom edge and body text for optimal presentation.
type: docs
weight: 80
url: /net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text.

```csharp
public double BottomMargin { get; set; }
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
