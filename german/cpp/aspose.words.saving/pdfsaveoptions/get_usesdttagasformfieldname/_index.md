---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName Methode"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName Methode. Gibt an, ob das Tag- oder Id‑Eigenschaft des SDT-Steuerelements als Name eines Formularfelds im PDF in C++ verwendet werden soll."
type: docs
weight: 32500
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Gibt an, ob das Tag‑ oder Id‑Eigenschaft des SDT‑Steuerelements als Name eines Formularfelds im PDF verwendet werden soll.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Hinweise


Der Standardwert ist **false**.

Wenn auf **false** gesetzt, wird die Id‑Eigenschaft des SDT-Steuerelements als Name eines Formularfelds im PDF verwendet.

Wenn auf **true** gesetzt, wird die Tag‑Eigenschaft des SDT-Steuerelements als Name eines Formularfelds im PDF verwendet.

Wenn auf **true** gesetzt und das Tag leer ist, wird die Id‑Eigenschaft als Formularfeldname verwendet.

Wenn auf **true** gesetzt und Tag‑Werte nicht eindeutig sind, werden doppelte Tag‑Werte geändert, um eindeutige PDF‑Formularfeldnamen zu erzeugen.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
