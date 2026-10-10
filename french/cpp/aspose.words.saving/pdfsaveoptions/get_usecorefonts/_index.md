---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts méthode"
linktitle: "get_UseCoreFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts méthode. Obtient ou définit une valeur déterminant s'il faut ou non substituer les polices TrueType Arial, Times New Roman, Courier New et Symbol par les polices PDF Type 1 de base en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Obtient ou définit une valeur déterminant s'il faut ou non remplacer les polices TrueType Arial, Times New Roman, Courier New et Symbol par les polices PDF Type 1 de base.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Remarques


La valeur par défaut est **false**. Lorsque cette valeur est définie sur **true**, les polices Arial, Times New Roman, Courier New et Symbol sont remplacées dans le document PDF par les polices Type 1 de base correspondantes.

Les polices PDF de base, ou leurs métriques de police et les polices de substitution appropriées, doivent être disponibles pour toute application de visualisation PDF.

Ce paramètre ne fonctionne que pour le texte encodé en ANSI (Windows‑1252). Le texte non‑ANSI sera écrit avec une police TrueType incorporée, quel que soit ce paramètre.

La conformité PDF/A et PDF/UA exige que toutes les polices soient incorporées. La valeur **false** sera utilisée automatiquement lors de l'enregistrement en PDF/A et PDF/UA.

Les polices de base ne sont pas prises en charge lors de l'enregistrement au format PDF 2.0. La valeur **false** sera utilisée automatiquement lors de l'enregistrement en PDF 2.0.

Cette option a une priorité plus élevée que l'option [FontEmbeddingMode](../get_fontembeddingmode/).
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
