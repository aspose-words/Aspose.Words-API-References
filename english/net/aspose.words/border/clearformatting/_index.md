---
title: Border.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: Reset your border properties to default with the Border ClearFormatting method. Simplify your design process and enhance your project's appearance!
type: docs
weight: 90
url: /net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

Resets border properties to default values.

```csharp
public void ClearFormatting()
```

## Remarks

When border properties are reset to default values, the border is invisible.

## Examples

Shows how to remove borders from a paragraph.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Each paragraph has an individual set of borders.
// We can access the settings for the appearance of these borders via the paragraph format object.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.That(borders[0].Color.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));
Assert.That(borders[0].LineWidth, Is.EqualTo(3.0d));
Assert.That(borders[0].LineStyle, Is.EqualTo(LineStyle.Single));
Assert.That(borders[0].IsVisible, Is.True);

// We can remove a border at once by running the ClearFormatting method. 
// Running this method on every border of a paragraph will remove all its borders.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.That(borders[0].Color.ToArgb(), Is.EqualTo(Color.Empty.ToArgb()));
Assert.That(borders[0].LineWidth, Is.EqualTo(0.0d));
Assert.That(borders[0].LineStyle, Is.EqualTo(LineStyle.None));
Assert.That(borders[0].IsVisible, Is.False);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### See Also

* class [Border](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
