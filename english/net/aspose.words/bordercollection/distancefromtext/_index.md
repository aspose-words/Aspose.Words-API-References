---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words for .NET API Reference
description: BorderCollection DistanceFromText property. Gets or sets distance of the border from text in points in C#.
type: docs
weight: 40
url: /net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Gets or sets distance of the border from text in points.

```csharp
public double DistanceFromText { get; set; }
```

## Remarks

Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.

## Examples

Shows how to create green wavy page border with a shadow.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### See Also

* class [BorderCollection](../)
* namespace [Aspose.Words](../../bordercollection/)
* assembly [Aspose.Words](../../../)
