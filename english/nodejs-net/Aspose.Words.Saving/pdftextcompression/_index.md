---
title: PdfTextCompression enumeration
linktitle: PdfTextCompression enumeration
articleTitle: PdfTextCompression enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PdfTextCompression enumeration. Specifies a type of compression applied to all content in the PDF file except images."
type: docs
weight: 730
url: /nodejs-net/aspose.words.saving/pdftextcompression/
---

## PdfTextCompression enumeration

Specifies a type of compression applied to all content in the PDF file except images.


### Members

| Name | Description |
| --- | --- |
| None | No compression. |
| Flate | Flate (ZIP) compression. |

### Examples

Shows how to apply text compression when saving a document to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

for (let i = 0; i < 100; i++)
  builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
          "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
// compression to text when we save the document to PDF.
// Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
// to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options.textCompression = pdfTextCompression;

doc.save(base.artifactsDir + "PdfSaveOptions.textCompression.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)

