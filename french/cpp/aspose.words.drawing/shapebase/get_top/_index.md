---
title: "Aspose::Words::Drawing::ShapeBase::get_Top méthode"
linktitle: "get_Top"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Top méthode. Obtient ou définit la position du bord supérieur du bloc contenant la forme en C++."
type: docs
weight: 52000
url: /fr/cpp/aspose.words.drawing/shapebase/get_top/
---
## ShapeBase::get_Top method


Obtient ou définit la position du bord supérieur du bloc contenant de la forme.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Top()
```

## Remarques


Pour une forme de niveau supérieur, la valeur est exprimée en points et relative à l’ancre de la forme.

Pour les formes dans un groupe, la valeur se trouve dans l'espace de coordonnées et les unités du groupe parent.

La valeur par défaut est 0.

N'a d'effet que pour les formes flottantes.

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

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
