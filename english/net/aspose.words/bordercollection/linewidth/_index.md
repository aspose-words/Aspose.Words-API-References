---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words for .NET
description: BorderCollection LineWidth property. Gets or sets the border width in points in C#.
type: docs
weight: 90
url: /net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Gets or sets the border width in points.

```csharp
public double LineWidth { get; set; }
```

## Remarks

Returns the width of the first border in the collection.

Sets the width of all borders in the collection excluding diagonal borders.

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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
