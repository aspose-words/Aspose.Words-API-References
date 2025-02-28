---
title: BorderCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the BorderCollection Count property to easily access the total number of borders, enhancing your design flexibility and efficiency.
type: docs
weight: 30
url: /net/aspose.words/bordercollection/count/
---
## BorderCollection.Count property

Gets the number of borders in the collection.

```csharp
public int Count { get; }
```

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

* class [BorderCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
