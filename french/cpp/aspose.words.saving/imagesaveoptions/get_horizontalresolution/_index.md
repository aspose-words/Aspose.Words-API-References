---
title: "Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution méthode"
linktitle: "get_HorizontalResolution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution méthode. Obtient ou définit la résolution horizontale des images générées, en points par pouce en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_horizontalresolution/
---
## ImageSaveOptions::get_HorizontalResolution method


Obtient ou définit la résolution horizontale des images générées, en points par pouce.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution() const
```

## Remarques


Cette propriété n'a d'effet que lors de l'enregistrement aux formats d'image raster et affecte la taille de sortie en pixels.

La valeur par défaut est 96.

## Exemples



Montre comment modifier l’image pendant qu’Aspose.Words convertit un document en une image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Lorsque nous enregistrons le document en tant qu’image, nous pouvons passer un objet SaveOptions à
// modifier l'image pendant que l'opération d'enregistrement la rend.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Nous pouvons ajuster ces propriétés pour modifier la luminosité et le contraste de l'image.
// Les deux sont sur une échelle de 0 à 1 et sont à 0,5 par défaut.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Nous pouvons ajuster la résolution horizontale et verticale avec ces propriétés.
// Cela affectera les dimensions de l'image.
// La valeur par défaut pour ces propriétés est 96,0, pour une résolution de 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Nous pouvons mettre à l'échelle l'image en utilisant cette propriété. La valeur par défaut est 1,0, pour un agrandissement de 100 %.
// Nous pouvons utiliser cette propriété pour annuler toute modification des dimensions de l'image que le changement de résolution entraînerait.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Voir aussi

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
