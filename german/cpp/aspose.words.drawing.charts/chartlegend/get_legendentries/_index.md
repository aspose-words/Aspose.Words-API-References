---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_LegendEntries-Methode"
linktitle: "get_LegendEntries"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_LegendEntries-Methode. Gibt eine Sammlung von Legendeinträgen für alle Serien und Trendlinien des übergeordneten Diagramms in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing.charts/chartlegend/get_legendentries/
---
## ChartLegend::get_LegendEntries method


Gibt eine Sammlung von Legendeneinträgen für alle Reihen und Trendlinien des übergeordneten Diagramms zurück.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntryCollection> Aspose::Words::Drawing::Charts::ChartLegend::get_LegendEntries() const
```


## Beispiele



Zeigt, wie man mit einem Legendeintrag für Diagrammserien arbeitet.
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

## Siehe auch

* Class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
