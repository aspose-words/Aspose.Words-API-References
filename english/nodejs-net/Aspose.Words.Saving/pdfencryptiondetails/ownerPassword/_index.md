---
title: PdfEncryptionDetails.ownerPassword property
linktitle: ownerPassword property
articleTitle: ownerPassword property
second_title: Aspose.Words for NodeJs
description: "PdfEncryptionDetails.ownerPassword property. Specifies the owner password for the encrypted PDF document."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/pdfencryptiondetails/ownerPassword/
---

## PdfEncryptionDetails.ownerPassword property

Specifies the owner password for the encrypted PDF document.


```js
get ownerPassword(): string
```

### Remarks

The owner password allows the user to open an encrypted PDF document without any access restrictions
specified in [PdfEncryptionDetails.permissions](../permissions/).

The owner password cannot be the same as the user password.




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

