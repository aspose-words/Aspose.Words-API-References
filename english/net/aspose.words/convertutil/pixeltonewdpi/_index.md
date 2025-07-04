---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words for .NET
description: Transform pixel resolutions effortlessly with ConvertUtil's PixelToNewDpi method. Achieve optimal image quality and precision for your projects.
type: docs
weight: 30
url: /net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Converts pixels from one resolution to another.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pixels | Double | The value to convert. |
| oldDpi | Double | The current dpi (dots per inch) resolution. |
| newDpi | Double | The new dpi (dots per inch) resolution. |

## Examples

Shows how to use convert points to pixels with default and custom resolution.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Define the size of the top margin of this section in pixels, according to a custom DPI.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.That(pageSetup.TopMargin, Is.EqualTo(37.5d).Within(0.01d));

// At the default DPI of 96, a pixel is 0.75 points.
Assert.That(ConvertUtil.PixelToPoint(1), Is.EqualTo(0.75d));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Set a new DPI and adjust the top margin value accordingly.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.That(pageSetup.TopMargin, Is.EqualTo(59.0d).Within(0.01d));

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### See Also

* class [ConvertUtil](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
