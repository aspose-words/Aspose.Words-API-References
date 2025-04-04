---
title: PdfSaveOptions.exportDocumentStructure property
linktitle: exportDocumentStructure property
articleTitle: exportDocumentStructure property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.exportDocumentStructure property. Gets or sets a value determining whether or not to export document structure."
type: docs
weight: 140
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/exportDocumentStructure/
---

## PdfSaveOptions.exportDocumentStructure property

Gets or sets a value determining whether or not to export document structure.


```js
get exportDocumentStructure(): boolean
```

### Remarks

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially
for the large documents.




### Examples

Shows how to preserve document structure elements, which can assist in programmatically interpreting our document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world!");
builder.paragraphFormat.style = doc.styles.at("Normal");
builder.write(
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();
// Set the "ExportDocumentStructure" property to "true" to make the document structure, such tags, available via the
// "Content" navigation pane of Adobe Acrobat at the cost of increased file size.
// Set the "ExportDocumentStructure" property to "false" to not export the document structure.
options.exportDocumentStructure = exportDocumentStructure;

// Suppose we export document structure while saving this document. In that case,
// we can open it using Adobe Acrobat and find tags for elements such as the heading
// and the next paragraph via "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc.save(base.artifactsDir + "PdfSaveOptions.exportDocumentStructure.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

