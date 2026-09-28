---
title: "Метод Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails"
linktitle: "get_EncryptionDetails"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails method. Получает или задает детали шифрования выходного PDF‑документа в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Получает или задаёт детали шифрования выходного PDF‑документа.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Примечания


Значение по умолчанию — **null**, и выходной документ не будет зашифрован. Когда это свойство задаётся действительным объектом [PdfEncryptionDetails](../../pdfencryptiondetails/), выходной PDF‑документ будет зашифрован.

Алгоритм шифрования AES‑128 используется при сохранении в соответствии с PDF 1.7 (включая PDF/UA‑1). Алгоритм шифрования AES‑256 используется при сохранении в соответствии с PDF 2.0.

Шифрование запрещено соответствием PDF/A. Эта опция будет игнорироваться при сохранении в PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## См. также

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
