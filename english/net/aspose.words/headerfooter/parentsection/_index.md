---
title: HeaderFooter.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words for .NET API Reference
description: HeaderFooter ParentSection property. Gets the parent section of this story in C#.
type: docs
weight: 60
url: /net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

Gets the parent section of this story.

```csharp
public Section ParentSection { get; }
```

## Remarks

`ParentSection` is equivalent to [`ParentNode`](../../node/parentnode/) casted to [`Section`](../../section/).

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
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

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
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// All the second section's header/footers are linked to the first section's headers/footers.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// In the third section, only the footer is linked to the first section's footer via the second section.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### See Also

* class [Section](../../section/)
* class [HeaderFooter](../)
* namespace [Aspose.Words](../../headerfooter/)
* assembly [Aspose.Words](../../../)
