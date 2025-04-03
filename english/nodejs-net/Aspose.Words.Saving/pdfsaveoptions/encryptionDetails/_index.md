---
title: PdfSaveOptions.encryptionDetails property
linktitle: encryptionDetails property
articleTitle: encryptionDetails property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.encryptionDetails property. Gets or sets the details for encrypting the output PDF document."
type: docs
weight: 130
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/encryptionDetails/
---

## PdfSaveOptions.encryptionDetails property

Gets or sets the details for encrypting the output PDF document.


```js
get encryptionDetails(): Aspose.Words.Saving.PdfEncryptionDetails
```

### Remarks

The default value is ``null`` and the output document will not be encrypted.
When this property is set to a valid [PdfEncryptionDetails](../../pdfencryptiondetails/) object,
then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1).
AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[PdfPermissions.ContentCopyForAccessibility](../../pdfpermissions/#ContentCopyForAccessibility) permission is required by PDF/UA compliance
if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[PdfPermissions.ContentCopyForAccessibility](../../pdfpermissions/#ContentCopyForAccessibility) permission is deprecated in PDF 2.0 format.
This permission will be ignored when saving to PDF 2.0.




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

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

