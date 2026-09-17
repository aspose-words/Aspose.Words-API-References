---
title: "Aspose::Words::Drawing::Fill::OneColorGradient méthode"
linktitle: "OneColorGradient"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Fill::OneColorGradient méthode. Définit le remplissage spécifié à un dégradé à une couleur en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words.drawing/fill/onecolorgradient/
---
## Fill::OneColorGradient(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) method


Définit le remplissage spécifié à un dégradé d'une seule couleur.

```cpp
void Aspose::Words::Drawing::Fill::OneColorGradient(Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant, double degree)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| style | Aspose::Words::Drawing::GradientStyle | Le style de dégradé [GradientStyle](../../gradientstyle/) |
| variant | Aspose::Words::Drawing::GradientVariant | La variante de dégradé [GradientVariant](../../gradientvariant/) |
| degré | double | Le degré du dégradé. Peut être une valeur de 0.0 (sombre) à 1.0 (clair). |

## Exemples



Montre comment remplir une forme avec des dégradés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Appliquer un remplissage en dégradé d'une couleur à la forme avec ForeColor du remplissage en dégradé.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Appliquer un remplissage en dégradé à deux couleurs à la forme.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Modifier BackColor du remplissage en dégradé.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Notez que les modifications "GradientAngle" pour "GradientStyle.FromCorner/GradientStyle.FromCenter"
// Le remplissage en dégradé n'a aucun effet, il ne fonctionnera que pour un dégradé linéaire.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Utilisez l'option de conformité pour définir la forme en utilisant DML si vous souhaitez obtenir "GradientStyle",
// "GradientVariant" et "GradientAngle" propriétés après la sauvegarde du document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Voir aussi

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::OneColorGradient(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) method


Définit le remplissage spécifié à un dégradé d'une seule couleur en utilisant la couleur spécifiée.

```cpp
void Aspose::Words::Drawing::Fill::OneColorGradient(System::Drawing::Color color, Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant, double degree)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| color | System::Drawing::Color | La couleur pour créer le dégradé. |
| style | Aspose::Words::Drawing::GradientStyle | Le style de dégradé [GradientStyle](../../gradientstyle/) |
| variant | Aspose::Words::Drawing::GradientVariant | La variante de dégradé [GradientVariant](../../gradientvariant/) |
| degré | double | Le degré du dégradé. Peut être une valeur de 0.0 (sombre) à 1.0 (clair). |

## Exemples



Montre comment remplir une forme avec des dégradés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Appliquer un remplissage en dégradé d'une couleur à la forme avec ForeColor du remplissage en dégradé.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Appliquer un remplissage en dégradé à deux couleurs à la forme.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Modifier BackColor du remplissage en dégradé.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Notez que les modifications "GradientAngle" pour "GradientStyle.FromCorner/GradientStyle.FromCenter"
// Le remplissage en dégradé n'a aucun effet, il ne fonctionnera que pour un dégradé linéaire.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Utilisez l'option de conformité pour définir la forme en utilisant DML si vous souhaitez obtenir "GradientStyle",
// "GradientVariant" et "GradientAngle" propriétés après la sauvegarde du document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Voir aussi

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
