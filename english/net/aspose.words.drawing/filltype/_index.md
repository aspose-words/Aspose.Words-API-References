---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.FillType enum. Specifies fill type for a fillable object in C#.
type: docs
weight: 1120
url: /net/aspose.words.drawing/filltype/
---
## FillType enumeration

Specifies fill type for a fillable object.

```csharp
public enum FillType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Solid | `1` | Solid fill. |
| Patterned | `2` | Patterned fill. |
| Gradient | `3` | Gradient fill. |
| Textured | `4` | Textured fill. |
| Background | `5` | Fill is the same as the background. |
| Picture | `6` | Picture fill. |

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
