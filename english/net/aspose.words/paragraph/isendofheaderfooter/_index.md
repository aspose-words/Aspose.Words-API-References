---
title: Paragraph.IsEndOfHeaderFooter
linktitle: IsEndOfHeaderFooter
articleTitle: IsEndOfHeaderFooter
second_title: Aspose.Words for .NET
description: Discover the IsEndOfHeaderFooter property for paragraphs. Easily determine if a paragraph is the last in a HeaderFooter, enhancing document structure.
type: docs
weight: 70
url: /net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

True if this paragraph is the last paragraph in the [`HeaderFooter`](../../headerfooter/) (main text story) of a [`Section`](../../section/); false otherwise.

```csharp
public bool IsEndOfHeaderFooter { get; }
```

## Examples

Shows how to create a header and a footer.

```csharp
Document doc = new Document();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.That(header.IsHeader, Is.True);
Assert.That(para.IsEndOfHeaderFooter, Is.True);

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.That(footer.IsHeader, Is.False);
Assert.That(para.IsEndOfHeaderFooter, Is.True);

Assert.That(para.ParentStory, Is.EqualTo(footer));
Assert.That(para.ParentSection, Is.EqualTo(footer.ParentSection));
Assert.That(header.ParentSection, Is.EqualTo(footer.ParentSection));

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
