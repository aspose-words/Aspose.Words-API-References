---
title: "Méthode Aspose::Words::Drawing::ShapeBase::get_CoordOrigin"
linktitle: "get_CoordOrigin"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ShapeBase::get_CoordOrigin. Les coordonnées du coin supérieur gauche du bloc contenant cette forme en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.drawing/shapebase/get_coordorigin/
---
## ShapeBase::get_CoordOrigin method


Les coordonnées du coin supérieur gauche du bloc contenant cette forme.

```cpp
System::Drawing::Point Aspose::Words::Drawing::ShapeBase::get_CoordOrigin()
```

## Remarques


La valeur par défaut est (0,0).

## Exemples



Montre comment créer et remplir une forme groupée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez une forme groupée. Une forme groupée peut afficher une collection de nœuds de formes enfants.
// Dans Microsoft Word, cliquer à l'intérieur de la bordure de la forme groupée ou sur l'une des formes enfants de la forme groupée va
// sélectionner toutes les autres formes enfants de ce groupe et nous permettre de mettre à l'échelle et de déplacer toutes les formes en même temps.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// Créez une forme groupée de 400 pt × 400 pt et placez‑la à l'origine des coordonnées des formes flottantes du document.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Définissez la taille du plan de coordonnées interne du groupe à 500 × 500 pt.
// Le coin supérieur gauche du groupe aura une coordonnée x et y de (0, 0),
// et le coin inférieur droit aura une coordonnée x et y de (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Définissez les coordonnées du coin supérieur gauche du groupe à (-250, -250).
// Le centre du groupe aura maintenant une valeur de coordonnée x et y de (0, 0),
// et le coin inférieur droit sera à (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Créez un rectangle qui affichera la bordure de cette forme de groupe et ajoutez-le au groupe.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// Une fois qu’une forme fait partie d’une forme de groupe, nous pouvons y accéder en tant que nœud enfant puis la modifier.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Créez une petite étoile rouge et insérez‑la dans le groupe.
// Alignez la forme avec l’origine des coordonnées du groupe, que nous avons déplacée au centre.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Insérez un rectangle, puis insérez un rectangle légèrement plus petit au même endroit avec une image.
// Les formes plus récentes que nous ajoutons au groupe se superposent aux formes plus anciennes. Le rectangle bleu clair chevauchera partiellement l’étoile rouge,
// et ensuite la forme avec l’image chevauchera le rectangle bleu clair, en l’utilisant comme cadre.
// Nous ne pouvons pas utiliser les propriétés "ZOrder" des formes pour manipuler leur arrangement au sein d’une forme de groupe.
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Insérez une zone de texte dans la forme de groupe. Définissez la propriété "Left" afin que le bord droit de la zone de texte
// touche la bordure droite de la forme de groupe. Définissez la propriété "Top" afin que la zone de texte se situe à l’extérieur
// de la bordure de la forme de groupe, avec sa taille supérieure alignée le long de la marge inférieure de la forme de groupe.
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


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
