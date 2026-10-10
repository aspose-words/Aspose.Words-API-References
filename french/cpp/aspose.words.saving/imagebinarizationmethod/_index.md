---
title: "Aspose::Words::Saving::ImageBinarizationMethod enum"
linktitle: "ImageBinarizationMethod"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageBinarizationMethod enum. Spécifie la méthode utilisée pour binariser l'image en C++."
type: docs
weight: 63000
url: /fr/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Spécifie la méthode utilisée pour binariser l’image.

```cpp
enum class ImageBinarizationMethod
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Threshold | 0 | Spécifie la méthode de seuil. |
| FloydSteinbergDithering | 1 | Spécifie le tramage en utilisant la méthode de diffusion d'erreur Floyd‑Steinberg. |


## Exemples



Montre comment définir le seuil d'erreur de binarisation TIFF lors de l'utilisation de la méthode Floyd‑Steinberg pour rendre une image TIFF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Lorsque nous enregistrons le document au format TIFF, nous pouvons passer un objet SaveOptions à
// ajuster le tramage que Aspose.Words appliquera lors du rendu de cette image.
// La valeur par défaut de la propriété "ThresholdForFloydSteinbergDithering" est 128.
// Des valeurs plus élevées tendent à produire des images plus sombres.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
