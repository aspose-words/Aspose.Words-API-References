---
title: PdfEncryptionDetails.userPassword property
linktitle: userPassword property
articleTitle: userPassword property
second_title: Aspose.Words for NodeJs
description: "PdfEncryptionDetails.userPassword property. Specifies the user password required for opening the encrypted PDF document."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/pdfencryptiondetails/userPassword/
---

## PdfEncryptionDetails.userPassword property

Specifies the user password required for opening the encrypted PDF document.


```js
get userPassword(): string
```

### Remarks

The user password will be required to open an encrypted PDF document for viewing. The permissions specified in
[PdfEncryptionDetails.permissions](../permissions/) will be enforced by the reader software.

The user password can be ``None`` or empty string, in this case no password will be required from the user when
opening the PDF document. The user password cannot be the same as the owner password.




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

