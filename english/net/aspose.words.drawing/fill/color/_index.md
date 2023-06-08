---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: Fill Color property. Gets or sets a Color object that represents the foreground color for the fill in C#.
type: docs
weight: 40
url: /net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Gets or sets a Color object that represents the foreground color for the fill.

```csharp
public Color Color { get; set; }
```

## Remarks

This property preserves the alpha component of the Color, unlike the [`ForeColor`](../forecolor/) property, which resets it to fully opaque color.

## Examples

Shows how to convert any of the fills back to solid fill.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Get Fill object for Font of the first Run.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Check Fill properties of the Font.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Change type of the fill to Solid with uniform green color.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
