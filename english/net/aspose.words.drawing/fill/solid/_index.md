---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words for .NET
description: Fill Solid method. Sets the fill to a uniform color in C#.
type: docs
weight: 250
url: /net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Sets the fill to a uniform color.

```csharp
public void Solid()
```

## Remarks

Use this method to convert any of the fills back to solid fill.

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Sets the fill to a specified uniform color.

```csharp
public void Solid(Color color)
```

## Remarks

Use this method to convert any of the fills back to solid fill.

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
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)
