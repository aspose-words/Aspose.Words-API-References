---
title: "Metodo Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType"
linktitle: "get_SeriesType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType. Ottiene il tipo di questa serie di grafico in C++."
type: docs
weight: 11500
url: /it/cpp/aspose.words.drawing.charts/chartseries/get_seriestype/
---
## ChartSeries::get_SeriesType method


Ottiene il tipo di questa serie di grafico.

```cpp
Aspose::Words::Drawing::Charts::ChartSeriesType Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType()
```


## Esempi



Mostra come rimuovere una serie di grafico specifica.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Rimuove tutte le serie di tipo Colonna.
for (int32_t i = chart->get_Series()->get_Count() - 1; i >= 0; i--)
{
    if (chart->get_Series()->idx_get(i)->get_SeriesType() == Aspose::Words::Drawing::Charts::ChartSeriesType::Column)
    {
        chart->get_Series()->RemoveAt(i);
    }
}

chart->get_Series()->Add(u"Aspose Series", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({5.6, 7.1, 2.9, 8.9}));

doc->Save(get_ArtifactsDir() + u"Charts.RemoveSpecificChartSeries.docx");
```

## Vedi anche

* Enum [ChartSeriesType](../../chartseriestype/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
