---
title: BorderCollection.Item
second_title: Aspose.Words for .NET API Reference
description: BorderCollection property. Retrieves a Border object by border type in C#.
type: docs
weight: 60
url: /net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

Retrieves a [`Border`](../../border/) object by border type.

```csharp
public Border this[BorderType borderType] { get; }
```

| Parameter | Description |
| --- | --- |
| borderType | A [`BorderType`](../../bordertype/) value that specifies the type of the border to retrieve. |

## Remarks

Note that not all borders are present for different document elements. This method throws an exception if you request a border not applicable to the current object.

## Examples

Shows how to decorate text with borders and shading.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### See Also

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* namespace [Aspose.Words](../../bordercollection/)
* assembly [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

Retrieves a [`Border`](../../border/) object by index.

```csharp
public Border this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | Zero-based index of the border to retrieve. |

## Examples

Shows how border collections can share elements.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Since we used the same border configuration while creating
// these paragraphs, their border collections share the same elements.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// After changing the line style of the borders in just the second paragraph,
// the border collections no longer share the same elements.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Changing the appearance of an empty border makes it visible.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### See Also

* class [Border](../../border/)
* class [BorderCollection](../)
* namespace [Aspose.Words](../../bordercollection/)
* assembly [Aspose.Words](../../../)
