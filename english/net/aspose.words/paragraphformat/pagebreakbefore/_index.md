---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words for .NET
description: Discover the ParagraphFormat PageBreakBefore property, easily control page breaks before paragraphs for enhanced document formatting and readability.
type: docs
weight: 270
url: /net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

True if a page break is forced before the paragraph.

```csharp
public bool PageBreakBefore { get; set; }
```

## Examples

Shows how to create paragraphs with page breaks at the beginning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set this flag to "true" to apply a page break to each paragraph's beginning
// that the document builder will create under this ParagraphFormat configuration.
// The first paragraph will not receive a page break.
// Leave this flag as "false" to start each new paragraph on the same page
// as the previous, provided there is sufficient space.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.That(layoutCollector.GetStartPageIndex(paragraphs[0]), Is.EqualTo(1));
    Assert.That(layoutCollector.GetStartPageIndex(paragraphs[1]), Is.EqualTo(2));
}
else
{
    Assert.That(layoutCollector.GetStartPageIndex(paragraphs[0]), Is.EqualTo(1));
    Assert.That(layoutCollector.GetStartPageIndex(paragraphs[1]), Is.EqualTo(1));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
