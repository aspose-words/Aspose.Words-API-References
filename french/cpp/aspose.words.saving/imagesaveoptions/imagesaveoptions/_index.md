---
title: "constructeur Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions"
linktitle: "ImageSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions constructeur. Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer des images rendues aux formats Tiff, Png, Bmp, Jpeg, Emf, Eps, WebP ou Svg en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer des images rendues aux formats [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../) ou [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Peut être [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/)[WebP](../) ou [Svg](../../../aspose.words/saveformat/) format. |

## Exemples



Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Définissez la propriété "JpegQuality" sur "10" pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus visibles.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Définissez la propriété "JpegQuality" sur "100" pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une taille de fichier accrue.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
