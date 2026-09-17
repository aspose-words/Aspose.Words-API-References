---
title: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution méthode"
linktitle: "set_Resolution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution méthode. Définit à la fois la résolution horizontale et verticale pour les images générées, en points par pouce en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Définit à la fois la résolution horizontale et verticale des images générées, en points par pouce.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Remarques


Cette propriété n’a d’effet que lors de l’enregistrement aux formats d’image raster.

## Exemples



Montre comment spécifier une résolution lors du rendu d'un document au format PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Définissez la propriété "Resolution" sur "72" pour rendre le document à 72 dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Définissez la propriété "Resolution" sur "300" pour rendre le document à 300 dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Voir aussi

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
