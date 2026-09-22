---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails yöntemi"
linktitle: "get_EncryptionDetails"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails yöntemi. Çıktı PDF belgesini şifrelemek için ayrıntıları alır veya ayarlar C++'da."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Çıktı PDF belgesinin şifrelenmesiyle ilgili ayrıntıları alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Açıklamalar


Varsayılan değer **null**'dır ve çıktı belge şifrelenmez. Bu özellik geçerli bir [PdfEncryptionDetails](../../pdfencryptiondetails/) nesnesine ayarlandığında, çıktı PDF belgesi şifrelenir.

PDF 1.7 uyumluluğuna (PDF/UA-1 dahil) kaydedilirken AES-128 şifreleme algoritması kullanılır. PDF 2.0 uyumluluğuna kaydedilirken AES-256 şifreleme algoritması kullanılır.

Şifreleme, PDF/A uyumluluğu tarafından yasaktır. Bu seçenek PDF/A'ya kaydedilirken yoksayılacaktır.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## Ayrıca Bakınız

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
