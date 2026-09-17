---
title: "méthode Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints"
linktitle: "get_BoundsInPoints"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints. Obtient la position et la taille du bloc conteneur de la forme en points, par rapport à l'ancre de la forme la plus élevée en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


Obtient l'emplacement et la taille du bloc contenant la forme en points, par rapport à l'ancre de la forme la plus haute.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## Exemples



Montre comment vérifier les limites du bloc conteneur de la forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Même si la ligne elle-même occupe peu d'espace sur la page du document,
// elle occupe un bloc conteneur rectangulaire, dont la taille peut être déterminée à l'aide des propriétés "Bounds".
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Créez une forme groupée, puis définissez la taille de son bloc conteneur à l'aide de la propriété "Bounds".
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Créez un rectangle, vérifiez la taille de son bloc de délimitation, puis ajoutez-le à la forme groupée.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Le plan de coordonnées de la forme groupée a son origine dans le coin supérieur gauche de son bloc conteneur,
// et les coordonnées x et y de (1000, 1000) dans le coin inférieur droit.
// Notre forme groupée mesure 250x250pt, donc chaque 4pt sur le plan de coordonnées de la forme groupée
// se traduit en 1pt dans le plan de coordonnées du corps du document.
// Chaque forme que nous insérons rétrécira également de taille d'un facteur de 4.
// La modification de la propriété "BoundsInPoints" de la forme reflétera cela.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Insérez une forme et placez-la en dehors des limites du bloc conteneur de la forme groupée.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// L'empreinte de la forme groupée dans le corps du document a augmenté, mais le bloc conteneur reste le même.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
