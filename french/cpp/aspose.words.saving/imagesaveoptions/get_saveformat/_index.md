---
title: "Méthode Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat. Spécifie le format dans lequel les pages ou formes du document rendu seront enregistrées si cet objet d’options d’enregistrement est utilisé. Peut être un raster Tiff, Png, Bmp, Jpeg ou un vecteur Emf, Eps, WebP, Svg en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


Spécifie le format dans lequel les pages ou formes du document rendu seront enregistrées si cet objet d’options d’enregistrement est utilisé. Peut être un raster [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/) ou un vecteur [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## Remarques


Le nombre d’autres options dépend du format sélectionné.

Il est également possible d’enregistrer en SVG à la fois via [ImageSaveOptions](../) et via [SvgSaveOptions](../../svgsaveoptions/).

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
