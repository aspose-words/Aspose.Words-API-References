---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering méthode"
linktitle: "get_ThresholdForFloydSteinbergDithering"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering méthode. Obtient ou définit le seuil qui détermine la valeur de l'erreur de binarisation dans la méthode Floyd‑Steinberg lorsque ImageBinarizationMethod est FloydSteinbergDithering en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method


Obtient ou définit le seuil qui détermine la valeur de l'erreur de binarisation dans la méthode Floyd‑Steinberg lorsque [ImageBinarizationMethod](../../imagebinarizationmethod/) est [FloydSteinbergDithering](../../imagebinarizationmethod/).

```cpp
uint8_t Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering() const
```

## Remarques


La valeur par défaut est 128.

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

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
