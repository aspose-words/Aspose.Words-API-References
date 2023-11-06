---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words for .NET
description: PageSetup PageHeight property. Returns or sets the height of the page in points in C#.
type: docs
weight: 310
url: /net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Returns or sets the height of the page in points.

```csharp
public double PageHeight { get; set; }
```

## Examples

Shows how to insert an image, and use it as a watermark.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert the image into the header so that it will be visible on every page.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Place the image at the center of the page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
