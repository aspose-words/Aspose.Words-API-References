---
title: HeaderFooter.IsLinkedToPrevious
linktitle: IsLinkedToPrevious
articleTitle: IsLinkedToPrevious
second_title: Aspose.Words for .NET
description: Discover how the IsLinkedToPrevious property enhances your document's headers and footers, ensuring seamless continuity across sections for better organization.
type: docs
weight: 40
url: /net/aspose.words/headerfooter/islinkedtoprevious/
---
## HeaderFooter.IsLinkedToPrevious property

True if this header or footer is linked to the corresponding header or footer in the previous section.

```csharp
public bool IsLinkedToPrevious { get; set; }
```

## Remarks

Default is `true`.

Note, when your link a header or footer, its contents is cleared.

## Examples

Shows how to link headers and footers between sections.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Move to the first section and create a header and a footer. By default,
// the header and the footer will only appear on pages in the section that contains them.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// We can link a section's headers/footers to the previous section's headers/footers
// to allow the linking section to display the linked section's headers/footers.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Each section will still have its own header/footer objects. When we link sections,
// the linking section will display the linked section's header/footers while keeping its own.
Assert.That(doc.Sections[1].HeadersFooters[0], Is.Not.EqualTo(doc.Sections[0].HeadersFooters[0]));
Assert.That(doc.Sections[1].HeadersFooters[0].ParentSection, Is.Not.EqualTo(doc.Sections[0].HeadersFooters[0].ParentSection));

// Link the headers/footers of the third section to the headers/footers of the second section.
// The second section already links to the first section's header/footers,
// so linking to the second section will create a link chain.
// The first, second, and now the third sections will all display the first section's headers.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// We can also select only a specific type of header/footer to link using this method.
// The third section now will have the same footer as the second and first sections, but not the header.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// The first section's header/footers cannot link themselves to anything because there is no previous section.
Assert.That(doc.Sections[0].HeadersFooters.Count, Is.EqualTo(2));
Assert.That(doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious), Is.EqualTo(2));

// All the second section's header/footers are linked to the first section's headers/footers.
Assert.That(doc.Sections[1].HeadersFooters.Count, Is.EqualTo(6));
Assert.That(doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious), Is.EqualTo(6));

// In the third section, only the footer is linked to the first section's footer via the second section.
Assert.That(doc.Sections[2].HeadersFooters.Count, Is.EqualTo(6));
Assert.That(doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious), Is.EqualTo(5));
Assert.That(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious, Is.True);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### See Also

* class [HeaderFooter](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
