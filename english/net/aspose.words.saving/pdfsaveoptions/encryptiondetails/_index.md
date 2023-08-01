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

### See Also

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
