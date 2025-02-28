---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words for .NET
description: Discover the BorderCollection LineStyle property to customize your design with flexible border styles. Enhance your project’s visual appeal effortlessly!
type: docs
weight: 80
url: /net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Gets or sets the border style.

```csharp
public LineStyle LineStyle { get; set; }
```

## Remarks

Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
