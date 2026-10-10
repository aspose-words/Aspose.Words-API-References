---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails méthode"
linktitle: "get_EncryptionDetails"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails method. Obtient ou définit les détails pour le chiffrement du document PDF de sortie en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Obtient ou définit les détails pour le chiffrement du document PDF de sortie.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Remarques


La valeur par défaut est **null** et le document de sortie ne sera pas chiffré. Lorsque cette propriété est définie sur un objet [PdfEncryptionDetails](../../pdfencryptiondetails/) valide, le document PDF de sortie sera alors chiffré.

L'algorithme de chiffrement AES-128 est utilisé lors de l'enregistrement conforme à PDF 1.7 (y compris PDF/UA-1). L'algorithme de chiffrement AES-256 est utilisé lors de l'enregistrement conforme à PDF 2.0.

Le chiffrement est interdit par la conformité PDF/A. Cette option sera ignorée lors de l'enregistrement au format PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## Voir aussi

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
