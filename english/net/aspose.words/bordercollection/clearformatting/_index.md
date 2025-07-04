---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: Discover how the BorderCollection ClearFormatting method effortlessly removes all object borders, enhancing your design with clean, crisp visuals.
type: docs
weight: 140
url: /net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Removes all borders of an object.

```csharp
public void ClearFormatting()
```

## Examples

Shows how to remove all borders from all paragraphs in a document.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// The first paragraph of this document has visible borders with these settings.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.That(firstParagraphBorders.Color.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));
Assert.That(firstParagraphBorders.LineStyle, Is.EqualTo(LineStyle.Single));
Assert.That(firstParagraphBorders.LineWidth, Is.EqualTo(3.0d));

// Use the "ClearFormatting" method on each paragraph to remove all borders.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.That(border.Color.ToArgb(), Is.EqualTo(Color.Empty.ToArgb()));
        Assert.That(border.LineStyle, Is.EqualTo(LineStyle.None));
        Assert.That(border.LineWidth, Is.EqualTo(0.0d));
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### See Also

* class [BorderCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
