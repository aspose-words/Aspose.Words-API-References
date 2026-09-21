---
title: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts method"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts method. Anger om skript ska genereras som efterliknar specifikt Microsoft Word‑formulärfältsbeteende i PDF. Standardvärdet är false i C++."
type: docs
weight: 18500
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Anger om skript ska genereras som efterliknar specifikt Microsoft Word-formulärfältbeteende i PDF. Standard är **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Anmärkningar


När detta alternativ är aktiverat genererar exportören PDF‑JavaScript‑åtgärder för att efterlikna Microsoft Word‑formulärfältsbeteende, såsom datum‑ och tidsformulärfält med formatering och valideringsregler.

När den är inställd på **true** exporteras stödjande beteende som PDF‑JavaScript‑åtgärder. När den är inställd på **false** genereras inga formulärfältsskript.

Skriptkörning beror på PDF‑visaren. Vissa PDF‑visare kan ignorera skript, begränsa skriptkörning eller kräva att användaren aktiverar JavaScript.

JavaScript‑åtgärder är förbjudna enligt PDF/A‑1, PDF/A‑2 och PDF/A‑3‑efterlevnad. Värdet **false** kommer att användas automatiskt i detta fall.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
