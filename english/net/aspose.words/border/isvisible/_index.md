---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words for .NET
description: Discover how the Border IsVisible property enhances your design by returning true when LineStyle is applied. Optimize your UI with this key feature!
type: docs
weight: 30
url: /net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Returns `true` if the [`LineStyle`](../linestyle/) is not None.

```csharp
public bool IsVisible { get; }
```

## Examples

Shows how to remove borders from a paragraph.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Each paragraph has an individual set of borders.
// We can access the settings for the appearance of these borders via the paragraph format object.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

// We can remove a border at once by running the ClearFormatting method. 
// Running this method on every border of a paragraph will remove all its borders.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### See Also

* class [Border](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
