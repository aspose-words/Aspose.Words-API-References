---
title: "Aspose::Words::Drawing::GradientStop classe"
linktitle: "GradientStop"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::GradientStop classe. Représente un arrêt de dégradé. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/gradientstop/
---
## GradientStop class


Représente un arrêt de dégradé. Pour en savoir plus, consultez l'article de documentation [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class GradientStop : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BaseColor](./get_basecolor/)() | Obtient une valeur représentant la couleur de l'arrêt de dégradé sans aucun modificateur. |
| [get_Color](./get_color/)() | Obtient ou définit une valeur représentant la couleur de l'arrêt de dégradé. |
| [get_Position](./get_position/)() const | Obtient ou définit une valeur représentant la position d'un arrêt dans le dégradé exprimée en pourcentage dans la plage de 0,0 à 1,0. |
| [get_Transparency](./get_transparency/)() const | Obtient ou définit une valeur représentant la transparence du remplissage du dégradé exprimée en pourcentage dans la plage de 0,0 à 1,0. |
| [GetType](./gettype/)() const override |  |
| [GradientStop](./gradientstop/)(System::Drawing::Color, double) | Initialise une nouvelle instance de la classe [GradientStop](./). |
| [GradientStop](./gradientstop/)(System::Drawing::Color, double, double) | Initialise une nouvelle instance de la classe [GradientStop](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime l'arrêt de dégradé du parent [GradientStopCollection](../gradientstopcollection/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::GradientStop::get_Color](./get_color/). |
| [set_Position](./set_position/)(double) | Définisseur pour [Aspose::Words::Drawing::GradientStop::get_Position](./get_position/). |
| [set_Transparency](./set_transparency/)(double) | Définisseur pour [Aspose::Words::Drawing::GradientStop::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment ajouter des arrêts de dégradé au remplissage du dégradé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// Obtenez la collection d'arrêts de dégradé.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// Modifiez le premier arrêt de dégradé.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Ajoutez un nouvel arrêt de dégradé à la fin de la collection.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// Supprimez l'arrêt de dégradé à l'indice 1.
gradientStops->RemoveAt(1);
// Et insérez un nouvel arrêt de dégradé au même indice 1.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Supprimez le dernier arrêt de dégradé dans la collection.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Utilisez l'option de conformité pour définir la forme à l'aide de DML
// si vous souhaitez obtenir la propriété "GradientStops" après l'enregistrement du document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
