---
title: "Aspose::Words::Drawing::ImageData::get_ImageSize méthode"
linktitle: "get_ImageSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageSize méthode. Obtient les informations sur la taille et la résolution de l'image en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.drawing/imagedata/get_imagesize/
---
## ImageData::get_ImageSize method


Obtient les informations sur la taille et la résolution de l'image.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageSize> Aspose::Words::Drawing::ImageData::get_ImageSize()
```

## Remarques


Si l'image n'est que liée et n'est pas stockée dans le document, renvoie une taille nulle.

## Exemples



Montre comment redimensionner une forme avec une image.
```cpp
// Lorsque nous insérons une image en utilisant la méthode "InsertImage", le constructeur met à l'échelle la forme qui affiche l'image afin que,
// Lorsque nous affichons le document avec un zoom de 100 % dans Microsoft Word, la forme affiche l'image à sa taille réelle.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Une image 400x400 créera un objet ImageData avec une taille d'image de 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Si les dimensions d'une forme correspondent aux dimensions des données d'image,
// alors la forme affiche l'image à sa taille d'origine.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Réduisez la taille globale de la forme de 50 %.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Les facteurs d'échelle s'appliquent à la fois à la largeur et à la hauteur simultanément pour préserver les proportions de la forme.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// Lorsque nous redimensionnons la forme, la taille des données d'image reste la même.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Nous pouvons nous référer aux dimensions des données d'image pour appliquer une mise à l'échelle basée sur la taille de l'image.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Voir aussi

* Class [ImageSize](../../imagesize/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
