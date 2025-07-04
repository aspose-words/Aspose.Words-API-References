---
title: Border.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: Aspose.Words for .NET
description: Discover the Border GetHashCode method, a powerful hash function that enhances data integrity and performance for your applications. Unlock its potential today!
type: docs
weight: 110
url: /net/aspose.words/border/gethashcode/
---
## Border.GetHashCode method

Serves as a hash function for this type.

```csharp
public override int GetHashCode()
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
    Assert.That(firstParagraphBorders[i].Equals(secondParagraphBorders[i]), Is.True);
    Assert.That(secondParagraphBorders[i].GetHashCode(), Is.EqualTo(firstParagraphBorders[i].GetHashCode()));
    Assert.That(firstParagraphBorders[i].IsVisible, Is.False);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// After changing the line style of the borders in just the second paragraph,
// the border collections no longer share the same elements.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.That(firstParagraphBorders[i].Equals(secondParagraphBorders[i]), Is.False);
    Assert.That(secondParagraphBorders[i].GetHashCode(), Is.Not.EqualTo(firstParagraphBorders[i].GetHashCode()));

    // Changing the appearance of an empty border makes it visible.
    Assert.That(secondParagraphBorders[i].IsVisible, Is.True);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### See Also

* class [Border](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
