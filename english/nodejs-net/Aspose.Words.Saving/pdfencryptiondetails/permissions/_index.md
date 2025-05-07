---
title: PdfEncryptionDetails.permissions property
linktitle: permissions property
articleTitle: permissions property
second_title: Aspose.Words for Node.js
description: "PdfEncryptionDetails.permissions property. Specifies the operations that are allowed to a user on an encrypted PDF document"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/pdfencryptiondetails/permissions/
---

## PdfEncryptionDetails.permissions property

Specifies the operations that are allowed to a user on an encrypted PDF document.
The default value is [PdfPermissions.DisallowAll](../../pdfpermissions/#DisallowAll).



```js
get permissions(): Aspose.Words.Saving.PdfPermissions
```

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
* class [PdfEncryptionDetails](../)

