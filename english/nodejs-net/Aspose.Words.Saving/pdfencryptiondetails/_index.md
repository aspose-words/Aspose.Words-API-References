---
title: PdfEncryptionDetails class
linktitle: PdfEncryptionDetails class
articleTitle: PdfEncryptionDetails class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PdfEncryptionDetails class. Contains details for encrypting and access permissions for a PDF document"
type: docs
weight: 650
url: /nodejs-net/Aspose.Words.Saving/pdfencryptiondetails/
---

## PdfEncryptionDetails class

Contains details for encrypting and access permissions for a PDF document.
To learn more, visit the [Protect or Encrypt a Document](https://docs.aspose.com/words/nodejs-net/protect-or-encrypt-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PdfEncryptionDetails(userPassword, ownerPassword)](./constructor/#string_string) | Initializes an instance of this class. |
| [PdfEncryptionDetails(userPassword, ownerPassword, permissions)](./constructor/#string_string_pdfpermissions) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [ownerPassword](./ownerPassword/) | Specifies the owner password for the encrypted PDF document. |
| [permissions](./permissions/) | Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [PdfPermissions.DisallowAll](../pdfpermissions/#DisallowAll). |
| [userPassword](./userPassword/) | Specifies the user password required for opening the encrypted PDF document. |

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

