---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields‑metod"
linktitle: "get_PreserveFormFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields‑metod. Anger om Microsoft Word-formulärfält ska bevaras som formulärfält i PDF eller konverteras till text. Standard är false i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Anger om Microsoft Word-formulärfält ska bevaras som formulärfält i PDF eller konverteras till text. Standard är **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Anmärkningar


Microsoft Word-formulärfält inkluderar textinmatning, rullgardinsmenyer och kryssrute‑kontroller.

När de är inställda på **false** exporteras dessa fält som text till PDF. När de är inställda på **true** exporteras dessa fält som PDF‑formulärfält.

När formulärfält exporteras till PDF som formulärfält kan viss formateringsförlust uppstå eftersom PDF‑formulärfält inte stöder alla funktioner för Microsoft Word‑formulärfält.

Dessutom beror utdata­storleken på innehållsstorleken eftersom redigerbara formulär i Microsoft Word är inline‑objekt.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
