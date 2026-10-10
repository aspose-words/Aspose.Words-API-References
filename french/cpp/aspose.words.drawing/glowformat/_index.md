---
title: "Aspose::Words::Drawing::GlowFormat classe"
linktitle: "GlowFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::GlowFormat classe. Représente le format de lueur pour un objet en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Représente le format de lueur d'un objet.

```cpp
class GlowFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Color](./get_color/)() | Obtient ou définit un objet **Color** qui représente la couleur d'un effet de lueur. La valeur par défaut est **Black**. |
| [get_Radius](./get_radius/)() | Obtient ou définit une valeur double qui représente la longueur du rayon d'un effet de lueur en points (pt). La valeur par défaut est 0.0. |
| [get_Transparency](./get_transparency/)() | Obtient ou définit le degré de transparence de l'effet de lueur comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). La valeur par défaut est 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime [GlowFormat](./) de l'objet parent. |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | Définisseur pour [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | Définisseur pour [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [Glow](../shapebase/get_glow/) pour accéder aux propriétés de lueur d'un objet. Vous ne créez pas d'instances de la classe [GlowFormat](./) directement.

## Exemples



Montre comment interagir avec l'effet de forme de lueur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
