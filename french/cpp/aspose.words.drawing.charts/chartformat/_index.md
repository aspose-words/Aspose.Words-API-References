---
title: "Aspose::Words::Drawing::Charts::ChartFormat classe"
linktitle: "ChartFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat classe. Représente le formatage d'un élément de graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Représente le formatage d'un élément de graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Fill](./get_fill/)() | Obtient le formatage du remplissage pour l'élément de graphique parent. |
| [get_IsDefined](./get_isdefined/)() | Obtient un indicateur indiquant si un format est défini. |
| [get_ShapeType](./get_shapetype/)() | Obtient ou définit le type de forme de l'élément de graphique parent. |
| [get_Stroke](./get_stroke/)() | Obtient le formatage de la ligne pour l'élément de graphique parent. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | Réinitialise le remplissage de l'élément de graphique pour qu'il ait la valeur par défaut. |
| static [Type](./type/)() |  |

## Exemples



Montre comment utiliser le formatage du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Supprimer les séries générées par défaut.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Formater l'arrière-plan du graphique.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Masquer les libellés des graduations de l'axe.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Formater le titre du graphique.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formater le titre de l'axe.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formater la légende.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
