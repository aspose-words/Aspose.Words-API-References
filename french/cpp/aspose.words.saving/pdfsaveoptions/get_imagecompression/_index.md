---
title: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression"
linktitle: "get_ImageCompression"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression. Spécifie le type de compression à utiliser pour toutes les images du document en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Spécifie le type de compression à utiliser pour toutes les images du document.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Remarques


Par défaut, c’est [Auto](../../pdfimagecompression/).

Utiliser [Jpeg](../../pdfimagecompression/) vous permet de contrôler la qualité des images dans le document de sortie via la propriété [JpegQuality](../get_jpegquality/).

Utiliser [Jpeg](../../pdfimagecompression/) offre la vitesse de conversion la plus rapide comparée aux performances des autres types de compression, mais dans ce cas, il s’agit d’une compression JPEG avec perte.

Utiliser [Auto](../../pdfimagecompression/) permet de contrôler la qualité du Jpeg dans le document de sortie via la propriété [JpegQuality](../get_jpegquality/), mais pour les autres formats, les données brutes des pixels sont extraites et enregistrées avec une compression Flate. Ce cas est plus lent que la conversion Jpeg mais sans perte.
## Voir aussi

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
