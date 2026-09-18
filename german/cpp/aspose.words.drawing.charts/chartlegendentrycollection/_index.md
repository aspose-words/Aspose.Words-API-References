---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntryCollection class"
linktitle: "ChartLegendEntryCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntryCollection class. Stellt eine Sammlung von Diagrammlegendeinträgen dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class


Stellt eine Sammlung von Diagrammlegende‑Einträgen dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartLegendEntryCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Gibt die Anzahl der [ChartLegendEntry](../chartlegendentry/) in dieser Sammlung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt den [ChartLegendEntry](../chartlegendentry/) für den angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
