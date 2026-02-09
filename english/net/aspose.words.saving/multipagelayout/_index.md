---
title: MultiPageLayout Class
linktitle: MultiPageLayout
articleTitle: MultiPageLayout
second_title: Aspose.Words for .NET
description: Defines layout rules for rendering multiple pages into one image using grid, horizontal or vertical style.
type: docs
weight: 6150
url: /net/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class

Defines a layout for rendering multiple pages into a single output.

```csharp
public sealed class MultiPageLayout
```

## Properties

| Name | Description |
| --- | --- |
| [BackColor](../../aspose.words.saving/multipagelayout/backcolor/) { get; set; } | Gets or sets the background color of the output. The default is Empty. |
| [BorderColor](../../aspose.words.saving/multipagelayout/bordercolor/) { get; set; } | Gets or sets the color of the pages border. The default is Empty. |
| [BorderWidth](../../aspose.words.saving/multipagelayout/borderwidth/) { get; set; } | Gets or sets the width of the pages border. The default is 0. |

## Methods

| Name | Description |
| --- | --- |
| static [Grid](../../aspose.words.saving/multipagelayout/grid/)(*int, float, float*) | Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns. |
| static [Horizontal](../../aspose.words.saving/multipagelayout/horizontal/)(*float*) | Creates a layout in which all specified pages are rendered horizontally side by side, left to right, in a single output. |
| static [SinglePage](../../aspose.words.saving/multipagelayout/singlepage/)() | Creates a layout that renders only the first of specified pages. |
| static [TiffFrames](../../aspose.words.saving/multipagelayout/tiffframes/)() | Creates a layout where each page is rendered as a separate frame in a multi-frame TIFF image. Applicable only to TIFF image formats. |
| static [Vertical](../../aspose.words.saving/multipagelayout/vertical/)(*float*) | Creates a layout where all specified pages are rendered vertically one below the other in a single output. |

## Remarks

Use one of the static factory methods to create a layout configuration.

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
