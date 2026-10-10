---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntryCollection class"
linktitle: "ChartLegendEntryCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntryCollection class. Rappresenta una raccolta di voci della legenda del grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class


Rappresenta una raccolta di voci della legenda del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegendEntryCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Restituisce il numero di [ChartLegendEntry](../chartlegendentry/) in questa raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce [ChartLegendEntry](../chartlegendentry/) per l'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come lavorare con una voce della legenda per le serie del grafico.
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

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
