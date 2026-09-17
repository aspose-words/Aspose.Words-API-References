---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects méthode"
linktitle: "get_BoundsWithEffects"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects méthode. Obtient l'étendue finale que cet objet forme possède après l'application des effets de dessin. La valeur est mesurée en points en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.drawing/shapebase/get_boundswitheffects/
---
## ShapeBase::get_BoundsWithEffects method


Obtient l'étendue finale que cet objet forme possède après l'application des effets de dessin. La valeur est mesurée en points.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects()
```


## Exemples



Montre comment vérifier comment les limites d'une forme sont affectées par les effets de forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Les deux formes sont identiques en termes de dimensions et de type de forme.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// La première forme n'a aucun effet, et la seconde possède une ombre et un contour épais.
// Ces effets rendent la taille de la silhouette de la seconde forme plus grande que celle de la première.
// Même si la taille du rectangle apparaît lorsque nous cliquons sur ces formes dans Microsoft Word,
// les limites extérieures visibles de la seconde forme sont affectées par l'ombre et le contour et sont donc plus grandes.
// Nous pouvons utiliser la méthode "AdjustWithEffects" pour voir la vraie taille de la forme.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Créez un objet RectangleF, représentant un rectangle,
// que nous pourrions éventuellement utiliser comme coordonnées et limites pour une forme.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Exécutez cette méthode pour obtenir la taille du rectangle ajustée pour tous nos effets de forme.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Comme la forme n'a aucun effet modifiant la bordure, ses dimensions de limites ne sont pas affectées.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Vérifiez l'étendue finale de la première forme, en points.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Les effets de forme ont légèrement déplacé le coin supérieur gauche apparent de la forme.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Les effets ont également affecté les dimensions visibles de la forme.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Les effets ont également affecté les limites visibles de la forme.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
