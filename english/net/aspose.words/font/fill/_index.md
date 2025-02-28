---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words for .NET
description: Discover the Font Fill property to enhance your text's appearance with customizable fill formatting for a polished, professional look.
type: docs
weight: 130
url: /net/aspose.words/font/fill/
---
## Font.Fill property

Gets fill formatting for the [`Font`](../).

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
