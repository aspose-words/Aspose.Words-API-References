---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: Discover the BorderCollection Color property to easily customize and manage border colors for your designs. Enhance your UI with vibrant options!
type: docs
weight: 20
url: /net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Gets or sets the border color.

```csharp
public Color Color { get; set; }
```

## Remarks

Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.

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
