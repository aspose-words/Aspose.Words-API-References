---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Drawing::Charts::ChartDataTable. Permet de spécifier les propriétés d'un tableau de données de graphique en C++."
type: docs
weight: 9500
url: /fr/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Permet de spécifier les propriétés d'un tableau de données de graphique.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Font](./get_font/)() | Fournit l'accès au formatage de police du tableau de données. |
| [get_Format](./get_format/)() | Fournit l'accès au remplissage de l'arrière-plan du texte et au formatage des bordures du tableau de données. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Obtient ou définit un indicateur indiquant si une bordure horizontale du tableau de données est affichée. La valeur par défaut est **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Obtient ou définit un indicateur indiquant si les clés de légende sont affichées dans le tableau de données. La valeur par défaut est **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Obtient ou définit un indicateur indiquant si une bordure de contour, c’est‑à‑dire une bordure autour des séries et des noms de catégorie, est affichée. La valeur par défaut est **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Obtient ou définit un indicateur indiquant si une bordure verticale du tableau de données est affichée. La valeur par défaut est **true**. |
| [get_Show](./get_show/)() const | Obtient ou définit un indicateur indiquant si le tableau de données sera affiché pour le graphique. La valeur par défaut est **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment afficher le tableau de données avec les données de séries du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
