---
title: PdfSaveOptions.exportLanguageToSpanTag property
linktitle: exportLanguageToSpanTag property
articleTitle: exportLanguageToSpanTag property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.exportLanguageToSpanTag property. Gets or sets a value determining whether or not to create a Span tag in the document structure to export the text language."
type: docs
weight: 150
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/exportLanguageToSpanTag/
---

## PdfSaveOptions.exportLanguageToSpanTag property

Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.


```js
get exportLanguageToSpanTag(): boolean
```

### Remarks

Default value is ``False`` and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is ``True`` "Span" tag is created for the text with non-default language
and "Lang" attribute is attached to this tag.

This value is ignored when [PdfSaveOptions.exportDocumentStructure](../exportDocumentStructure/) is ``False``. 




### Examples

Shows how to create a "Span" tag in the document structure to export the text language.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");
builder.writeln("Hola mundo!");

let saveOptions = new aw.Saving.PdfSaveOptions();
// Note, when "ExportDocumentStructure" is false, "ExportLanguageToSpanTag" is ignored.
saveOptions.exportDocumentStructure = true;
saveOptions.exportLanguageToSpanTag = true;

doc.save(base.artifactsDir + "PdfSaveOptions.exportLanguageToSpanTag.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

