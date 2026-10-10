---
title: "Méthode get_IsWashout de Aspose::Words::ImageWatermarkOptions"
linktitle: "get_IsWashout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode get_IsWashout de Aspose::Words::ImageWatermarkOptions. Obtient ou définit une valeur booléenne qui est responsable de l'effet de délavage du filigrane. La valeur par défaut est true en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Obtient ou définit une valeur booléenne qui est responsable de l'effet de blanchiment du filigrane. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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
