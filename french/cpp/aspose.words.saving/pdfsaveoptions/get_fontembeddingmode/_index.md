---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode méthode"
linktitle: "get_FontEmbeddingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode méthode. Spécifie le mode d'incorporation des polices en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Spécifie le mode d'incorporation des polices.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Remarques


La valeur par défaut est [EmbedAll](../../pdffontembeddingmode/).

Ce paramètre ne fonctionne que pour le texte encodé en ANSI (Windows‑1252). Si le document contient du texte non ANSI, les polices correspondantes seront incorporées quel que soit ce paramètre.

La conformité PDF/A et PDF/UA exige que toutes les polices soient incorporées. La valeur [EmbedAll](../../pdffontembeddingmode/) sera utilisée automatiquement lors de l’enregistrement au format PDF/A et PDF/UA.
## Voir aussi

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
