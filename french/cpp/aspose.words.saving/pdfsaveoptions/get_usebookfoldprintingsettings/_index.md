---
title: "méthode Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings. Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d’impression en livret, si elle est spécifiée via MultiplePages en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_usebookfoldprintingsettings/
---
## PdfSaveOptions::get_UseBookFoldPrintingSettings method


Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression en livret, si elle est spécifiée via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Remarques


Si cette option est spécifiée, [PageSet](../../fixedpagesaveoptions/get_pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression en livret ne sont pas spécifiés dans la configuration de la page, cette option n'aura aucun effet.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
