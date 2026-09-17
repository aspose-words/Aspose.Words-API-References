---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden méthode"
linktitle: "get_IsHidden"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden méthode. Obtient ou définit une valeur indiquant si cet élément est masqué dans la légende du graphique. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing.charts/chartlegendentry/get_ishidden/
---
## ChartLegendEntry::get_IsHidden method


Obtient ou définit une valeur indiquant si cette entrée est masquée dans la légende du graphique. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden() const
```


## Exemples



Montre comment travailler avec une entrée de légende pour une série de graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"});

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
series->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));
series->Add(u"Series 4", categories, System::MakeArray<double>({0, 0}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntryCollection> legendEntries = chart->get_Legend()->get_LegendEntries();
legendEntries->idx_get(3)->set_IsHidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.LegendEntries.docx");
```

## Voir aussi

* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
