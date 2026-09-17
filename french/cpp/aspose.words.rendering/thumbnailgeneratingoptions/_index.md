---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. Peut être utilisé pour spécifier des options supplémentaires lors de la génération d'une vignette pour un document en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Peut être utilisé pour spécifier des options supplémentaires lors de la génération d'une miniature d'un document.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Spécifie s'il faut générer la vignette à partir de la première page du document ou de la première image. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Taille de la vignette générée en pixels. La valeur par défaut est 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Définisseur pour [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Définisseur pour [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
