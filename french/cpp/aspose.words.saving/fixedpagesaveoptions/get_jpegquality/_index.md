---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality méthode"
linktitle: "get_JpegQuality"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality méthode. Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document Html en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document Html.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Remarques


N'a d'effet que lorsqu'un document contient des images JPEG.

Utilisez cette propriété pour obtenir ou définir la qualité des images dans un document lors de l'enregistrement au format page fixe. La valeur peut varier de 0 à 100 où 0 signifie la pire qualité mais la compression maximale et 100 signifie la meilleure qualité mais la compression minimale.

La valeur par défaut est 95.

## Exemples



Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Définissez la propriété "JpegQuality" sur "10" pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus visibles.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Définissez la propriété "JpegQuality" sur "100" pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une taille de fichier accrue.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Voir aussi

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
