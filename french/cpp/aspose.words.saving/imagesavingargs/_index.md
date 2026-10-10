---
title: "Aspose::Words::Saving::ImageSavingArgs classe"
linktitle: "ImageSavingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSavingArgs classe. Fournit des données pour l'événement ImageSaving(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Fournit des données pour l'événement [ImageSaving()](../iimagesavingcallback/imagesaving/). Pour en savoir plus, consultez l'article de documentation [Enregistrer un document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ImageSavingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Obtient l'objet [ShapeBase](../../aspose.words.drawing/shapebase/) correspondant à la forme ou au groupe de formes qui est sur le point d'être enregistré. |
| [get_Document](./get_document/)() | Obtient l'objet document qui est actuellement en cours d'enregistrement. |
| [get_ImageFileName](./get_imagefilename/)() const | Obtient ou définit le nom de fichier (sans le chemin) où l'image sera enregistrée. |
| [get_ImageStream](./get_imagestream/)() const | Permet de spécifier le flux où l'image sera enregistrée. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Renvoie **true** si l'image actuelle est disponible pour l'exportation. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une image. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Définisseur pour [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définisseur de [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Définisseur de [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Remarques


Par défaut, lorsque Aspose.Words enregistre un document au format HTML, il enregistre chaque image dans un fichier séparé. Aspose.Words utilise le nom de fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque image trouvée dans le document.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Pour appliquer votre propre logique de génération des noms de fichiers d'image, utilisez les propriétés [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) et [IsImageAvailable](./get_isimageavailable/).

Pour enregistrer les images dans des flux au lieu de fichiers, utilisez la propriété [ImageStream](./get_imagestream/).
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
