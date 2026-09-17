---
title: "Méthode Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage"
linktitle: "get_GenerateFromFirstPage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage. Spécifie si la vignette doit être générée à partir de la première page du document ou de la première image en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Spécifie s'il faut générer la vignette à partir de la première page du document ou de la première image.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
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
