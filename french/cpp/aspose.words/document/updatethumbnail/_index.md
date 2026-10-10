---
title: "Aspose::Words::Document::UpdateThumbnail méthode"
linktitle: "UpdateThumbnail"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::UpdateThumbnail méthode. Met à jour la vignette du document en utilisant les options par défaut en C++."
type: docs
weight: 100000
url: /fr/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Met à jour la [Vignette](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) du document en utilisant les options par défaut.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Met à jour la [Vignette](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) du document selon les options spécifiées.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | Les options de génération à utiliser. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
