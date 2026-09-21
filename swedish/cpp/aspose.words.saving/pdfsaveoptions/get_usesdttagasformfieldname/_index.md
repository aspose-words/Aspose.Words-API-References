---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName metod"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName metod. Anger om SDT‑kontrollens Tag‑ eller Id‑egenskap ska användas som namn på formulärfält i PDF i C++."
type: docs
weight: 32500
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Anger om SDT‑kontrollens Tag‑ eller Id‑egenskap ska användas som namn på formulärfält i PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Anmärkningar


Standardvärdet är **false**.

När den sätts till **false**, används SDT‑kontrollens Id‑egenskap som namn på formulärfält i PDF.

När den sätts till **true**, används SDT‑kontrollens Tag‑egenskap som namn på formulärfält i PDF.

Om den sätts till **true** och Tag är tomt, kommer Id‑egenskapen att användas som namn på formulärfältet.

Om den sätts till **true** och Tag‑värdena inte är unika, kommer dubblett‑Tag‑värden att ändras för att skapa unika PDF‑formulärfältsnamn.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
