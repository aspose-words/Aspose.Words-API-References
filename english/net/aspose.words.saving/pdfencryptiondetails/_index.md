---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.PdfEncryptionDetails class. Contains details for encrypting and access permissions for a PDF document in C#.
type: docs
weight: 5280
url: /net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contains details for encrypting and access permissions for a PDF document.

To learn more, visit the [Protect or Encrypt a Document](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) documentation article.

```csharp
public class PdfEncryptionDetails
```

## Constructors

| Name | Description |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/)(*string, string*) | Initializes an instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Specifies the owner password for the encrypted PDF document. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is DisallowAll. |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Specifies the user password required for opening the encrypted PDF document. |

## Examples

Shows how to set permissions on a saved PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Start by disallowing all permissions.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Extend permissions to allow the editing of annotations.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Enable encryption via the "EncryptionDetails" property.
saveOptions.EncryptionDetails = encryptionDetails;

// When we open this document, we will need to provide the password before accessing its contents.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
