---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts méthode"
linktitle: "get_EmbedFullFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts méthode. Contrôle la façon dont les polices sont incorporées dans les documents PDF résultants en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Contrôle la façon dont les polices sont incorporées dans les documents PDF résultants.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Remarques


La valeur par défaut est **false**, ce qui signifie que les polices sont sous‑échantillonnées avant l'incorporation. Le sous‑échantillonnage est utile si vous souhaitez garder la taille du fichier de sortie plus petite. Le sous‑échantillonnage supprime tous les glyphes inutilisés d'une police.

Lorsque cette valeur est définie sur **true**, un fichier de police complet est incorporé dans le PDF sans sous‑échantillonnage. Cela entraînera des fichiers de sortie plus volumineux, mais peut être une option utile lorsque vous souhaitez modifier le PDF résultant plus tard (par ex. ajouter plus de texte).

Certaines polices sont volumineuses (plusieurs mégaoctets) et les incorporer sans sous‑échantillonnage entraînera de gros documents de sortie.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
