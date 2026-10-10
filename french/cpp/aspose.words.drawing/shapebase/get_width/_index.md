---
title: "Méthode Aspose::Words::Drawing::ShapeBase::get_Width"
linktitle: "get_Width"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ShapeBase::get_Width. Obtient ou définit la largeur du bloc contenant de la forme en C++."
type: docs
weight: 54000
url: /fr/cpp/aspose.words.drawing/shapebase/get_width/
---
## ShapeBase::get_Width method


Obtient ou définit la largeur du bloc contenant de la forme.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Width()
```

## Remarques


Pour une forme de niveau supérieur, la valeur est en points.

Pour les formes dans un groupe, la valeur se trouve dans l'espace de coordonnées et les unités du groupe parent.

La valeur par défaut est 0.

## Exemples



Montre comment insérer une image flottante et spécifier sa position et sa taille.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configurez la propriété "RelativeHorizontalPosition" de la forme pour traiter la valeur de la propriété "Left"
// comme la distance horizontale de la forme, en points, depuis le côté gauche de la page.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Définissez la distance horizontale de la forme depuis le côté gauche de la page à 100.
shape->set_Left(100);

// Utilisez la propriété "RelativeVerticalPosition" de manière similaire pour positionner la forme à 80 pt sous le haut de la page.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Définissez la hauteur de la forme, ce qui ajustera automatiquement la largeur pour préserver les dimensions.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Les propriétés "Bottom" et "Right" contiennent respectivement les bords inférieur et droit de l'image.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
