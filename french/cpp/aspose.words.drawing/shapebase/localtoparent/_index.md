---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent méthode"
linktitle: "LocalToParent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent méthode. Convertit une valeur de l'espace de coordonnées local vers l'espace de coordonnées de la forme parent en C++."
type: docs
weight: 61000
url: /fr/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Convertit une valeur de l'espace de coordonnées local vers l'espace de coordonnées de la forme parent.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Exemples



Montre comment traduire la position des coordonnées x et y sur le plan de coordonnées d’une forme vers une position sur le plan de coordonnées de la forme parent.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez une forme de groupe, et placez‑la 100 points en dessous et à droite de
// le point d’origine des coordonnées x et Y du document.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Utilisez la méthode "LocalToParent" pour déterminer que (0, 0) sur les coordonnées x et y internes du groupe
// se trouve sur (100, 100) du système de coordonnées de sa forme parent. Le parent de la forme de groupe est le document lui‑même.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// Par défaut, le plan de coordonnées interne d’une forme a le coin supérieur gauche à (0, 0),
// et le coin inférieur droit à (1000, 1000). En raison de sa taille, notre forme de groupe couvre une zone de 500pt x 500pt
// dans le plan du document. Cela signifie qu’un déplacement de 1pt sur le plan de coordonnées du document se traduira
// en un déplacement de 2pts sur le plan de coordonnées de la forme de groupe.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Déplacez l'origine des axes x et y de la forme de groupe du coin supérieur gauche vers le centre.
// Cela décalera davantage les coordonnées internes du groupe par rapport aux coordonnées du document.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Modifier l'échelle du plan de coordonnées affectera également les emplacements relatifs.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Si nous souhaitons ajouter une forme à ce groupe tout en définissant son emplacement en fonction d'un emplacement dans le document,
// nous devrons d'abord confirmer un emplacement dans la forme de groupe qui correspondra à l'emplacement du document.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
