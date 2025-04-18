---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words for .NET
description: Discover how the UserPassword property enhances PDF security by requiring a password for access, ensuring your documents stay protected and confidential.
type: docs
weight: 40
url: /net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Specifies the user password required for opening the encrypted PDF document.

```csharp
public string UserPassword { get; set; }
```

## Remarks

The user password will be required to open an encrypted PDF document for viewing. The permissions specified in [`Permissions`](../permissions/) will be enforced by the reader software.

The user password can be `null` or empty string, in this case no password will be required from the user when opening the PDF document. The user password cannot be the same as the owner password.

## Examples

Shows how to set permissions on a saved PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Extend permissions to allow the editing of annotations.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Enable encryption via the "EncryptionDetails" property.
saveOptions.EncryptionDetails = encryptionDetails;

// When we open this document, we will need to provide the password before accessing its contents.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### See Also

* class [PdfEncryptionDetails](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
