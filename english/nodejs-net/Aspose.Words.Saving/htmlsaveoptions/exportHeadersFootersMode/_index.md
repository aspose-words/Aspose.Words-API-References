---
title: HtmlSaveOptions.exportHeadersFootersMode property
linktitle: exportHeadersFootersMode property
articleTitle: exportHeadersFootersMode property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.exportHeadersFootersMode property. Specifies how headers and footers are output to HTML, MHTML or EPUB"
type: docs
weight: 160
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportHeadersFootersMode/
---

## HtmlSaveOptions.exportHeadersFootersMode property

Specifies how headers and footers are output to HTML, MHTML or EPUB.
Default value is [ExportHeadersFootersMode.PerSection](../../exportheadersfootersmode/#PerSection) for HTML/MHTML
and [ExportHeadersFootersMode.None](../../exportheadersfootersmode/#None) for EPUB.



```js
get exportHeadersFootersMode(): Aspose.Words.Saving.ExportHeadersFootersMode
```

### Remarks

It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [ExportHeadersFootersMode.PerSection](../../exportheadersfootersmode/#PerSection), Aspose.Words exports
only primary headers and footers at the beginning and the end of each section.

When it is [ExportHeadersFootersMode.FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/#FirstSectionHeaderLastSectionFooter)
only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property
to [ExportHeadersFootersMode.None](../../exportheadersfootersmode/#None).




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

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

