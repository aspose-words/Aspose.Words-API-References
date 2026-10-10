---
title: "Méthode Aspose::Words::ImageWatermarkOptions::get_Scale"
linktitle: "get_Scale"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ImageWatermarkOptions::get_Scale. Obtient ou définit le facteur d'échelle exprimé comme une fraction de l'image. La valeur par défaut est 0 - auto en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Obtient ou définit le facteur d'échelle exprimé comme une fraction de l'image. La valeur par défaut est 0 - auto.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Remarques


Les valeurs valides vont de 0 à 65,5 inclus.

Le redimensionnement automatique signifie que le filigrane sera mis à l'échelle à sa largeur maximale et à sa hauteur maximale par rapport aux marges de la page.

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

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
