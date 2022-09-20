---
title: Item
second_title: Aspose.Words for .NET API Reference
description: Retrieves a HeaderFooter at the given index.
type: docs
weight: 10
url: /net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Retrieves a **HeaderFooter** at the given index.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the collection. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

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

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* namespace [Aspose.Words](../../headerfootercollection/)
* assembly [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Retrieves a **HeaderFooter** of the specified type.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parameter | Description |
| --- | --- |
| headerFooterType | A [`HeaderFooterType`](../../headerfootertype/) value that specifies the type of the header/footer to retrieve. |

## Remarks

Returns null if the header/footer of the specified type is not found.

## Examples

Shows how to replace text in a document's footer.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Shows how to delete all footers from a document.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterate through each section and remove footers of every kind.
foreach (Section section in doc.OfType<Section>())
{
    // There are three kinds of footer and header types.
    // 1 -  The "First" header/footer, which only appears on the first page of a section.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

    // 3 -  The "Even" header/footer, which appears on even pages. 
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### See Also

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* namespace [Aspose.Words](../../headerfootercollection/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
