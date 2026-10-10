---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName metodo"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName metodo. Specifica se utilizzare il Tag o la proprietà Id del controllo SDT come nome del campo modulo nel PDF in C++."
type: docs
weight: 32500
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Specifica se utilizzare il Tag o la proprietà Id del controllo SDT come nome del campo modulo nel PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Note


Il valore predefinito è **false**.

Quando impostato su **false**, la proprietà Id del controllo SDT è usata come nome del campo modulo nel PDF.

Quando impostato su **true**, la proprietà Tag del controllo SDT è usata come nome del campo modulo nel PDF.

Se impostato su **true** e il Tag è vuoto, la proprietà Id sarà usata come nome del campo modulo.

Se impostato su **true** e i valori Tag non sono unici, i valori Tag duplicati saranno modificati per creare nomi di campo modulo PDF unici.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
