---
title: ExportHeadersFootersMode enumeration
linktitle: ExportHeadersFootersMode enumeration
articleTitle: ExportHeadersFootersMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.ExportHeadersFootersMode enumeration. Specifies how headers and footers are exported to HTML, MHTML or EPUB."
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Saving/exportheadersfootersmode/
---

## ExportHeadersFootersMode enumeration

Specifies how headers and footers are exported to HTML, MHTML or EPUB.


### Members

| Name | Description |
| --- | --- |
| None | Headers and footers are not exported. |
| PerSection | Primary headers and footers are exported at the beginning and the end of each section. |
| FirstSectionHeaderLastSectionFooter | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| FirstPageHeaderFooterPerSection | First page header and footer are exported at the beginning and the end of each section. |

### Examples

Shows how to omit headers/footers when saving a document to HTML.

```js
let doc = new aw.Document(base.myDir + "Header and footer types.docx");

// This document contains headers and footers. We can access them via the "HeadersFooters" collection.
expect(doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.HeaderFirst).getText().trim()).toEqual("First header");

// Formats such as .html do not split the document into pages, so headers/footers will not function the same way
// they would when we open the document as a .docx using Microsoft Word.
// If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
// We can use a SaveOptions object to omit headers/footers while converting to html.
let saveOptions = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
saveOptions.exportHeadersFootersMode = aw.Saving.ExportHeadersFootersMode.None;

doc.save(base.artifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Open our saved document and verify that it does not contain the header's text
doc = new aw.Document(base.artifactsDir + "HeaderFooter.ExportMode.html");

expect(doc.range.text.includes("First header")).toEqual(false);
```

### See Also

* module [Aspose.Words.Saving](../)
* property [HtmlSaveOptions.exportHeadersFootersMode](../htmlsaveoptions/exportHeadersFootersMode/)

