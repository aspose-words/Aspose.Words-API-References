---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails Methode"
linktitle: "get_EncryptionDetails"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails Methode. Liest oder setzt die Details für die Verschlüsselung des ausgegebenen PDF-Dokuments in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Liest oder legt die Details für die Verschlüsselung des Ausgabepdf‑Dokuments fest.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Hinweise


Der Standardwert ist **null** und das Ausgabedokument wird nicht verschlüsselt. Wenn diese Eigenschaft auf ein gültiges [PdfEncryptionDetails](../../pdfencryptiondetails/) Objekt gesetzt wird, wird das Ausgabepdf-Dokument verschlüsselt.

Der AES-128-Verschlüsselungsalgorithmus wird verwendet, wenn nach PDF 1.7‑basierten Vorgaben (einschließlich PDF/UA-1) gespeichert wird. Der AES-256-Verschlüsselungsalgorithmus wird verwendet, wenn nach PDF 2.0‑basierten Vorgaben gespeichert wird.

Verschlüsselung ist durch PDF/A‑Konformität untersagt. Diese Option wird beim Speichern nach PDF/A ignoriert.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## Siehe auch

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
