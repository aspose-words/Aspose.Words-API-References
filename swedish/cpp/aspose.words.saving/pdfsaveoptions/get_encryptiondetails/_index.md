---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails metod"
linktitle: "get_EncryptionDetails"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails metod. Hämtar eller anger detaljerna för att kryptera utdata‑PDF‑dokumentet i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Hämtar eller anger detaljerna för kryptering av utdata-PDF-dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Anmärkningar


Standardvärdet är **null** och utdata‑dokumentet kommer inte att krypteras. När den här egenskapen sätts till ett giltigt [PdfEncryptionDetails](../../pdfencryptiondetails/)‑objekt, kommer utdata‑PDF‑dokumentet att krypteras.

AES‑128‑krypteringsalgoritmen används vid sparande till PDF 1.7‑baserad efterlevnad (inklusive PDF/UA‑1). AES‑256‑krypteringsalgoritmen används vid sparande till PDF 2.0‑baserad efterlevnad.

Kryptering är förbjuden enligt PDF/A‑efterlevnad. Detta alternativ kommer att ignoreras vid sparande till PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## Se även

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
