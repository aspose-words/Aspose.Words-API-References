---
title: "Aspose::Words::ImageWatermarkOptions classe"
linktitle: "ImageWatermarkOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::ImageWatermarkOptions. Contient des options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec une image. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Contient les options pouvant être spécifiées lors de l'ajout d'un filigrane avec une image. Pour en savoir plus, consultez l'article de documentation [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class ImageWatermarkOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Obtient ou définit une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. La valeur par défaut est **true**. |
| [get_Scale](./get_scale/)() const | Obtient ou définit le facteur d'échelle exprimé comme une fraction de l'image. La valeur par défaut est 0 - auto. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Définisseur pour [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Définisseur pour [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifiez l'apparence du filigrane d'image avec un objet ImageWatermarkOptions,
// puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Nous disposons d'options différentes pour insérer une image.
// Utilisez l'une des méthodes suivantes pour ajouter un filigrane d'image.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
