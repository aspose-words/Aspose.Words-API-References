---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds méthode"
linktitle: "get_Bounds"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds méthode. Obtient ou définit l'emplacement et la taille du bloc contenant de la forme en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


Obtient ou définit l'emplacement et la taille du bloc contenant la forme.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## Remarques


Ignore le verrouillage du rapport d'aspect lors du réglage.

Pour une forme de niveau supérieur, la valeur est exprimée en points et relative à l’ancre de la forme.

Pour les formes dans un groupe, la valeur se trouve dans l'espace de coordonnées et les unités du groupe parent.

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
