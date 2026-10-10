---
title: "méthode Aspose::Words::Saving::ImageSaveOptions::get_ImageSize"
linktitle: "get_ImageSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize méthode. Obtient ou définit la taille d'une image générée en pixels en C++."
type: docs
weight: 7500
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Obtient ou définit la taille d'une image générée en pixels.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Remarques


Cette propriété n’a d’effet que lors de l’enregistrement aux formats d’image raster.

La valeur par défaut est (0 x 0), ce qui signifie que la taille de l'image générée sera calculée en fonction de la taille de l'image en points, de la résolution spécifiée et de l'échelle.

## Exemples



Montre comment rendre chaque page d'un document en une image TIFF distincte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Définissez la propriété "PageSet" au numéro de la première page à partir de
    // à partir de laquelle commencer le rendu du document.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exporter la page à 2325x5325 pixels et 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## Voir aussi

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
