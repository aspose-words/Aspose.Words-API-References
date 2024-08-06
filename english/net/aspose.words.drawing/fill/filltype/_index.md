---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words for .NET
description: Fill FillType property. Gets a fill type in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Gets a fill type.

```csharp
public FillType FillType { get; }
```

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
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### See Also

* enum [FillType](../../filltype/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
