---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden método"
linktitle: "get_IsHidden"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden método. Obtiene o establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing.charts/chartlegendentry/get_ishidden/
---
## ChartLegendEntry::get_IsHidden method


Obtiene o establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden() const
```


## Ejemplos



Muestra cómo trabajar con una entrada de leyenda para series de gráfico.
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

## Ver también

* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
