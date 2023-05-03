---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
second_title: Aspose.Words for .NET API Reference
description: BorderCollection ClearFormatting method. Removes all borders of an object in C#.
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

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Use the "ClearFormatting" method on each paragraph to remove all borders.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### See Also

* class [BorderCollection](../)
* namespace [Aspose.Words](../../bordercollection/)
* assembly [Aspose.Words](../../../)
