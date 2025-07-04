---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: Aspose.Words for .NET
description: Discover the Story AppendParagraph method, effortlessly create and append a Paragraph object with customizable text for seamless document enhancement.
type: docs
weight: 60
url: /net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

A shortcut method that creates a [`Paragraph`](../../paragraph/) object with optional text and appends it to the end of this object.

```csharp
public Paragraph AppendParagraph(string text)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | String | The text for the paragraph. Can be `null` or empty string. |

### Return Value

The newly created and appended paragraph.

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
