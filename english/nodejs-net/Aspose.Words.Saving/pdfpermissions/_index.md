---
title: PdfPermissions enumeration
linktitle: PdfPermissions enumeration
articleTitle: PdfPermissions enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PdfPermissions enumeration. Specifies the operations that are allowed to a user on an encrypted PDF document."
type: docs
weight: 710
url: /nodejs-net/aspose.words.saving/pdfpermissions/
---

## PdfPermissions enumeration

Specifies the operations that are allowed to a user on an encrypted PDF document.


### Members

| Name | Description |
| --- | --- |
| DisallowAll | Disallows all operations on the PDF document. This is the default value. |
| AllowAll | Allows all operations on the PDF document. |
| ContentCopy | Copy or otherwise extract text and graphics from the document by operations other than that controlled by [PdfPermissions.ContentCopyForAccessibility](./#ContentCopyForAccessibility). |
| ContentCopyForAccessibility | Extract text and graphics (in support of accessibility to users with disabilities or for other purposes). |
| ModifyContents | Modify the contents of the document by operations other than those controlled by [PdfPermissions.ModifyAnnotations](./#ModifyAnnotations), [PdfPermissions.FillIn](./#FillIn), and [PdfPermissions.DocumentAssembly](./#DocumentAssembly). |
| ModifyAnnotations | Add or modify text annotations, fill in interactive form fields, and, if [PdfPermissions.ModifyContents](./#ModifyContents) is also set, create or modify interactive form fields (including signature fields). |
| FillIn | Fill in existing interactive form fields (including signature fields), even if [PdfPermissions.ModifyContents](./#ModifyContents) is clear. |
| DocumentAssembly | Assemble the document (insert, rotate, or delete pages and create document outline items or thumbnail images), even if [PdfPermissions.ModifyContents](./#ModifyContents) is clear. |
| Printing | Print the document (possibly not at the highest quality level, depending on whether [PdfPermissions.HighResolutionPrinting](./#HighResolutionPrinting) is also set). |
| HighResolutionPrinting | Print the document to a representation from which a faithful digital copy of the PDF content could be generated, based on an implementation-dependent algorithm. When this flag is clear (and [PdfPermissions.Printing](./#Printing) is set), printing shall be limited to a low-level representation of the appearance, possibly of degraded quality. |

### Examples

Shows how to set permissions on a saved PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

// Extend permissions to allow the editing of annotations.
let encryptionDetails =
  new aw.Saving.PdfEncryptionDetails("password", '', aw.Saving.PdfPermissions.ModifyAnnotations | aw.Saving.PdfPermissions.DocumentAssembly);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();
// Enable encryption via the "EncryptionDetails" property.
saveOptions.encryptionDetails = encryptionDetails;

// When we open this document, we will need to provide the password before accessing its contents.
doc.save(base.artifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

