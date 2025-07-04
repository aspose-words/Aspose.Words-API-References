---
title: ImageSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words for .NET
description: Specifies how multiple document pages are arranged in a single image for accurate visual output.
type: docs
weight: 100
url: /net/aspose.words.saving/imagesaveoptions/pagelayout/
---
## ImageSaveOptions.PageLayout property

Gets or sets the layout used when rendering multiple pages into a single output.

```csharp
public MultiPageLayout PageLayout { get; set; }
```

## Remarks

Use one of the factory methods of [`MultiPageLayout`](../../multipagelayout/) to configure this property.

For Tiff the default value is [`TiffFrames`](../../multipagelayout/tiffframes/). For other formats the default value is [`SinglePage`](../../multipagelayout/singlepage/).

This property has effect only when saving to the following formats: Jpeg, Gif, Png, Bmp, Tiff, WebP

## Examples

Shows how to save the document into JPG image with multi-page layout settings.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Set up a grid layout with:
// - 3 columns per row.
// - 10pts spacing between pages (horizontal and vertical).
options.PageLayout = MultiPageLayout.Grid(3, 10, 10);

// Alternative layouts:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Customize the background and border.
options.PageLayout.BackColor = Color.LightGray;
options.PageLayout.BorderColor = Color.Blue;
options.PageLayout.BorderWidth = 2;

doc.Save(ArtifactsDir + "ImageSaveOptions.GridLayout.jpg", options);
```

### See Also

* class [MultiPageLayout](../../multipagelayout/)
* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
