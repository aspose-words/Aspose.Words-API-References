---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails"
linktitle: "get_EncryptionDetails"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails método. Obtiene o establece los detalles para encriptar el documento PDF de salida en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


Obtiene o establece los detalles para encriptar el documento PDF de salida.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## Observaciones


El valor predeterminado es **null** y el documento de salida no se encriptará. Cuando esta propiedad se establece en un objeto [PdfEncryptionDetails](../../pdfencryptiondetails/) válido, entonces el documento PDF de salida se encriptará.

Se utiliza el algoritmo de cifrado AES-128 al guardar con cumplimiento basado en PDF 1.7 (incluyendo PDF/UA-1). Se utiliza el algoritmo de cifrado AES-256 al guardar con cumplimiento basado en PDF 2.0.

El cifrado está prohibido por el cumplimiento PDF/A. Esta opción se ignorará al guardar en PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## Ver también

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
