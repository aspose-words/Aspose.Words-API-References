---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words ExportHeadersFootersMode enum for seamless HTML, MHTML, or EPUB header and footer exports. Optimize your document conversion today!
type: docs
weight: 5780
url: /net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Specifies how headers and footers are exported to HTML, MHTML or EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Headers and footers are not exported. |
| PerSection | `1` | Primary headers and footers are exported at the beginning and the end of each section. |
| FirstSectionHeaderLastSectionFooter | `2` | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| FirstPageHeaderFooterPerSection | `3` | First page header and footer are exported at the beginning and the end of each section. |

## Examples

Shows how to omit headers/footers when saving a document to HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// This document contains headers and footers. We can access them via the "HeadersFooters" collection.
Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim(), Is.EqualTo("First header"));

// Formats such as .html do not split the document into pages, so headers/footers will not function the same way
// they would when we open the document as a .docx using Microsoft Word.
// If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
// We can use a SaveOptions object to omit headers/footers while converting to html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Open our saved document and verify that it does not contain the header's text
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.That(doc.Range.Text.Contains("First header"), Is.False);
```

### See Also

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
