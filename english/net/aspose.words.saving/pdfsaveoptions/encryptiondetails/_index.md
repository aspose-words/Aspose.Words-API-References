---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words for .NET
description: PdfSaveOptions EncryptionDetails property. Gets or sets the details for encrypting the output PDF document in C#.
type: docs
weight: 130
url: /net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Gets or sets the details for encrypting the output PDF document.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Remarks

The default value is `null` and the output document will not be encrypted. When this property is set to a valid [`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1). AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

ContentCopyForAccessibility permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

ContentCopyForAccessibility permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0.

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
