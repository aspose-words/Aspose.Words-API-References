---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode méthode"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode méthode. Spécifie comment l'espace colorimétrique sera sélectionné pour les images du document PDF en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Spécifie comment l’espace colorimétrique sera sélectionné pour les images du document PDF.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Remarques


La valeur par défaut est [Auto](../../pdfimagecolorspaceexportmode/).

Si la valeur [SimpleCmyk](../../pdfimagecolorspaceexportmode/) est spécifiée, l'option [ImageCompression](../get_imagecompression/) est ignorée et la compression Flate est utilisée pour toutes les images du document.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## Voir aussi

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
