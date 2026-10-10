---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails metodo"
linktitle: "get_EncryptionDetails"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails method. Ottiene o imposta i dettagli per la crittografia del documento PDF di output in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Ottiene o imposta i dettagli per la crittografia del documento PDF di output.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Note


Il valore predefinito è **null** e il documento di output non verrà crittografato. Quando questa proprietà è impostata su un oggetto [PdfEncryptionDetails](../../pdfencryptiondetails/) valido, il documento PDF di output verrà crittografato.

L'algoritmo di crittografia AES-128 viene utilizzato quando si salva in conformità PDF 1.7 (incluso PDF/UA-1). L'algoritmo di crittografia AES-256 viene utilizzato quando si salva in conformità PDF 2.0.

La crittografia è vietata dalla conformità PDF/A. Questa opzione verrà ignorata quando si salva in PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## Vedi anche

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
