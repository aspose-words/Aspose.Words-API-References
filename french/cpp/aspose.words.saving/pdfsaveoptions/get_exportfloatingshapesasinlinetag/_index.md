---
title: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag. Obtient ou définit une valeur déterminant si les formes flottantes sont exportées en tant que balises en ligne dans la structure du document en C++."
type: docs
weight: 16500
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


Obtient ou définit une valeur déterminant si les formes flottantes sont exportées en tant que balises en ligne dans la structure du document.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## Remarques


La valeur par défaut est **false** et les formes flottantes seront exportées en tant que balises de niveau bloc, placées après le paragraphe auquel elles sont ancrées.

Lorsque la valeur est **true**, les formes flottantes seront exportées en tant que balises en ligne, placées à l’intérieur du paragraphe où elles sont ancrées.

Cette valeur est ignorée lorsque [ExportDocumentStructure](../get_exportdocumentstructure/) est **false**.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
