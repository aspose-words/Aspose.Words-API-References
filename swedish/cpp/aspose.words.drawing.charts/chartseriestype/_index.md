---
title: "Aspose::Words::Drawing::Charts::ChartSeriesType enum"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesType enum. Anger en typ av diagramserie i C++."
type: docs
weight: 27500
url: /sv/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Anger en typ av en diagramserie.

```cpp
enum class ChartSeriesType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Area | 0 | Representerar en Area-diagramserie. |
| AreaStacked | 1 | Representerar en staplad Area-diagramserie. |
| AreaPercentStacked | 2 | Representerar en 100 % staplad Area-diagramserie. |
| Area3D | 3 | Representerar en 3D Area-diagramserie. |
| Area3DStacked | 4 | Representerar en 3D staplad Area-diagramserie. |
| Area3DPercentStacked | 5 | Representerar en 3D 100 % staplad Area-diagramserie. |
| Bar | 6 | Representerar en stapeldiagramserie. |
| BarStacked | 7 | Representerar en staplad stapeldiagramserie. |
| BarPercentStacked | 8 | Representerar en 100 % staplad stapeldiagramserie. |
| Bar3D | 9 | Representerar en 3D stapeldiagramserie. |
| Bar3DStacked | 10 | Representerar en 3D staplad stapeldiagramserie. |
| Bar3DPercentStacked | 11 | Representerar en 3D 100 % staplad stapeldiagramserie. |
| Bubble | 12 | Representerar en bubbeldiagramserie. |
| Bubble3D | 13 | Representerar en 3D bubbeldiagramserie. |
| Kolumn | 14 | Representerar en kolumndiagramserie. |
| ColumnStacked | 15 | Representerar en staplad kolumndiagramserie. |
| ColumnPercentStacked | 16 | Representerar en 100% staplad kolumndiagramserie. |
| Column3D | 17 | Representerar en 3D kolumndiagramserie. |
| Column3DStacked | 18 | Representerar en 3D staplad kolumndiagramserie. |
| Column3DPercentStacked | 19 | Representerar en 3D 100% staplad kolumndiagramserie. |
| Column3DClustered | 20 | Representerar en 3D grupperad kolumndiagramserie. |
| Doughnut | 21 | Representerar en munkdiagramserie. |
| Linje | 22 | Representerar en linjediagramserie. |
| LineStacked | 23 | Representerar en staplad linjediagramserie. |
| LinePercentStacked | 24 | Representerar en 100% staplad linjediagramserie. |
| Line3D | 25 | Representerar en 3D linjediagramserie. |
| Pie | 26 | Representerar en cirkeldiagramserie. |
| Pie3D | 27 | Representerar en 3D cirkeldiagramserie. |
| PieOfBar | 28 | Representerar en cirkel-i-stapeldiagramserie. |
| PieOfPie | 29 | Representerar en cirkel-i-cirkeldiagramserie. |
| Radar | 30 | Representerar en radardiagramserie. |
| Scatter | 31 | Representerar en spridningsdiagramserie. |
| Aktie | 32 | Representerar en aktiediagramserie. |
| Yta | 33 | Representerar en ytdiagramserie. |
| Surface3D | 34 | Representerar en 3D ytdiagramserie. |
| Träddiagram | 35 | Representerar en trädmappdiagramserie. |
| Sunburst | 36 | Representerar en solutbrottsdiagramserie. |
| Histogram | 37 | Representerar en histogramdiagramserie. |
| Pareto | 38 | Representerar en Pareto-diagramserie. |
| ParetoLine | 39 | Representerar en Pareto Line-diagramserie. |
| BoxAndWhisker | 40 | Representerar en Box and Whisker-diagramserie. |
| Vattenfall | 41 | Representerar en Waterfall-diagramserie. |
| Tratt | 42 | Representerar en Funnel-diagramserie. |
| RegionMap | 43 | Representerar en Region Map-diagramserie. |


## Exempel



Visar hur man tar bort en specifik diagramserie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Ta bort alla serier av typen Column.
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

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
