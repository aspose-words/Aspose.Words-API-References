---
title: "Méthode Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod"
linktitle: "get_TiffBinarizationMethod"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod. Obtient ou définit la méthode utilisée lors de la conversion des images au format 1 bpp lorsque SaveFormat est Tiff et TiffCompression est égal à Ccitt3 ou Ccitt4 en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Obtient ou définit la méthode utilisée lors de la conversion des images au format 1 bpp lorsque [SaveFormat](../get_saveformat/) est [Tiff](../../../aspose.words/saveformat/) et [TiffCompression](../get_tiffcompression/) est égal à [Ccitt3](../../tiffcompression/) ou [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Remarques


La valeur par défaut est [Threshold](../../imagebinarizationmethod/).

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
