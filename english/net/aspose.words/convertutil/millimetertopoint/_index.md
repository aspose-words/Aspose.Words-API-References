---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
second_title: Aspose.Words for .NET API Reference
description: ConvertUtil MillimeterToPoint method. Converts millimeters to points in C#.
type: docs
weight: 20
url: /net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Converts millimeters to points.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | Double | The value to convert. |

## Remarks

1 inch equals 25.4 millimeters. 1 inch equals 72 points.

## Examples

Shows how to specify page properties in millimeters.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a more familiar measurement unit,
// such as millimeters when defining boundaries.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// A centimeter is approximately 28.3 points.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Add content to demonstrate the new margins.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### See Also

* class [ConvertUtil](../)
* namespace [Aspose.Words](../../convertutil/)
* assembly [Aspose.Words](../../../)
