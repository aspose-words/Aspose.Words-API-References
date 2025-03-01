---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: Discover the BorderCollection Shadow property to enhance your designs. Easily control border shadows for a modern, stylish look in your projects!
type: docs
weight: 110
url: /net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Gets or sets a value indicating whether the border has a shadow.

```csharp
public bool Shadow { get; set; }
```

## Remarks

Gets the value from the first border in the collection.

Sets the value for all borders in the collection excluding diagonal borders.

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
