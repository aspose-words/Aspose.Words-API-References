---
title: Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails method
linktitle: get_EncryptionDetails
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails method. Gets or sets the details for encrypting the output PDF document in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Gets or sets the details for encrypting the output PDF document.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Remarks


The default value is **null** and the output document will not be encrypted. When this property is set to a valid [PdfEncryptionDetails](../../pdfencryptiondetails/) object, then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1). AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## See Also

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
