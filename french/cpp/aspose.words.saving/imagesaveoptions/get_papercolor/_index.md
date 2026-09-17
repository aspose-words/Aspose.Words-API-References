---
title: "Méthode Aspose::Words::Saving::ImageSaveOptions::get_PaperColor"
linktitle: "get_PaperColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::ImageSaveOptions::get_PaperColor. Obtient ou définit la couleur d’arrière‑plan (papier) des images générées. La valeur par défaut est White en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Obtient ou définit la couleur d'arrière-plan (papier) des images générées. La valeur par défaut est **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Remarques


Lors du rendu des pages d’un document qui spécifie sa propre couleur d’arrière‑plan, la couleur d’arrière‑plan du document remplacera la couleur spécifiée par cette propriété.

## Exemples



Rend une page d'un document Word en image avec un arrière-plan transparent ou coloré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Définissez la propriété "PaperColor" sur une couleur transparente pour appliquer une transparente
// arrière-plan au document lors du rendu en image.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Définissez la propriété "PaperColor" sur une couleur opaque pour appliquer cette couleur
// comme arrière-plan du document lors du rendu en image.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## Voir aussi

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
