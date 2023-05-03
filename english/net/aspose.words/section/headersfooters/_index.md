---
title: Section.HeadersFooters
linktitle: HeadersFooters
articleTitle: HeadersFooters
second_title: Aspose.Words for .NET API Reference
description: Section HeadersFooters property. Provides access to the headers and footers nodes of the section in C#.
type: docs
weight: 30
url: /net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

Provides access to the headers and footers nodes of the section.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

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

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* namespace [Aspose.Words](../../section/)
* assembly [Aspose.Words](../../../)
