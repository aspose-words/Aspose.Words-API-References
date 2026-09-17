---
title: "Méthode Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize"
linktitle: "get_ThumbnailSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize. Taille de la vignette générée en pixels. La valeur par défaut est 600x900 en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


Taille de la vignette générée en pixels. La valeur par défaut est 600x900.

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
```


## Exemples



Montre comment mettre à jour la vignette d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Il existe deux façons de définir une image de vignette lors de l'enregistrement d'un document au format .epub.
// 1 -  Utilisez la première page du document :
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Utilisez la première image trouvée dans le document :
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## Voir aussi

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
