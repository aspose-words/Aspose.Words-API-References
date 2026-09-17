---
title: "Aspose::Words::Drawing::GradientStopCollection classe"
linktitle: "GradientStopCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::GradientStopCollection classe. Contient une collection d'objets GradientStop. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class


Contient une collection d'objets [GradientStop](../gradientstop/). Pour en savoir plus, consultez l'article de documentation [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class GradientStopCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::GradientStop>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Ajoute un [GradientStop](../gradientstop/) spécifié à un dégradé. |
| [get_Count](./get_count/)() | Obtient une valeur entière indiquant le nombre d'éléments dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un énumérateur qui parcourt la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit un objet [GradientStop](../gradientstop/) dans la collection. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Obtient ou définit un objet [GradientStop](../gradientstop/) dans la collection. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Insère un [GradientStop](../gradientstop/) dans la collection à un indice spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Supprime un [GradientStop](../gradientstop/) spécifié de la collection. |
| [RemoveAt](./removeat/)(int32_t) | Supprime un [GradientStop](../gradientstop/) de la collection à un indice spécifié. |
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
