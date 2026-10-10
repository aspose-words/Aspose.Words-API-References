---
title: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality méthode"
linktitle: "get_JpegQuality"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality méthode. Obtient ou définit une valeur déterminant la qualité des images JPEG à l'intérieur du document PDF en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Obtient ou définit une valeur déterminant la qualité des images JPEG à l'intérieur du document PDF.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Remarques


La valeur par défaut est 100.

Cette propriété est utilisée conjointement avec l'option [ImageCompression](../get_imagecompression/).

N'a d'effet que lorsqu'un document contient des images JPEG.

Utilisez cette propriété pour obtenir ou définir la qualité des images à l'intérieur d'un document lors de l'enregistrement au format PDF. La valeur peut varier de 0 à 100 où 0 signifie la pire qualité mais une compression maximale et 100 signifie la meilleure qualité mais une compression minimale. Si la qualité est de 100 et que l'image source est JPEG, cela signifie aucune compression – les octets originaux seront enregistrés.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
