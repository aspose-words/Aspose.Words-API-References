---
title: "Méthode Aspose::Words::Drawing::ImageSize::get_VerticalResolution"
linktitle: "get_VerticalResolution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ImageSize::get_VerticalResolution. Obtient la résolution verticale en DPI en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing/imagesize/get_verticalresolution/
---
## ImageSize::get_VerticalResolution method


Obtient la résolution verticale en DPI.

```cpp
double Aspose::Words::Drawing::ImageSize::get_VerticalResolution() const
```


## Exemples



Montre comment lire les propriétés d'une image dans une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une forme dans le document qui contient une image provenant de notre système de fichiers local.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Si la forme contient une image, sa propriété ImageData sera valide,
// et elle contiendra un objet ImageSize.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// L'objet ImageSize contient des informations en lecture seule sur l'image à l'intérieur de la forme.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Nous pouvons baser la taille de la forme sur la taille de son image pour éviter d'étirer l'image.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## Voir aussi

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
