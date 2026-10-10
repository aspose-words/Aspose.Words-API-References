---
title: "méthode Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact. Obtient ou définit une valeur déterminant si un graphique de paragraphe doit être marqué comme un artefact en C++."
type: docs
weight: 17500
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


Obtient ou définit une valeur déterminant si un graphique de paragraphe doit être marqué comme un artefact.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## Remarques


La valeur par défaut est **false** et les graphiques de paragraphe (soulignements, emphase de texte, etc.) seront marqués comme "Span" dans la structure logique du document.

Lorsque la valeur est **true**, les graphiques de paragraphe seront marqués comme "Artifact".

Cette valeur est ignorée lorsque [ExportDocumentStructure](../get_exportdocumentstructure/) est **false**.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
