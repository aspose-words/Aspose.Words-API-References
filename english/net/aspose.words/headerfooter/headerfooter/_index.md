---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words for .NET
description: Design stunning headers and footers effortlessly with our intuitive constructor. Customize your website's look for a unique, professional touch!
type: docs
weight: 10
url: /net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Creates a new header or footer of the specified type.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |
| headerFooterType | HeaderFooterType | A [`HeaderFooterType`](../headerfootertype/) value that specifies the type of the header or footer. |

## Remarks

When [`HeaderFooter`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To append [`HeaderFooter`](../) to a [`Section`](../../section/) use [`InsertAfter`](../../compositenode/insertafter/), [`InsertBefore`](../../compositenode/insertbefore/), or [`HeadersFooters`](../../section/headersfooters/) property and methods [`Add`](../../nodecollection/add/), [`Insert`](../../nodecollection/insert/).

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
