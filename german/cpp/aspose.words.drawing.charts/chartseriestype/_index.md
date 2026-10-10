---
title: "Aspose::Words::Drawing::Charts::ChartSeriesType enum"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesType enum. Gibt einen Typ einer Diagrammserie in C++ an."
type: docs
weight: 27500
url: /de/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Gibt einen Typ einer Diagrammreihe an.

```cpp
enum class ChartSeriesType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Area | 0 | Stellt eine Flächendiagrammserie dar. |
| AreaStacked | 1 | Stellt eine gestapelte Flächendiagrammserie dar. |
| AreaPercentStacked | 2 | Stellt eine zu 100% gestapelte Flächendiagrammserie dar. |
| Area3D | 3 | Stellt eine 3D-Flächendiagrammserie dar. |
| Area3DStacked | 4 | Stellt eine 3D-gestapelte Flächendiagrammserie dar. |
| Area3DPercentStacked | 5 | Stellt eine 3D zu 100% gestapelte Flächendiagrammserie dar. |
| Bar | 6 | Stellt eine Balkendiagrammserie dar. |
| BarStacked | 7 | Stellt eine gestapelte Balkendiagrammserie dar. |
| BarPercentStacked | 8 | Stellt eine zu 100% gestapelte Balkendiagrammserie dar. |
| Bar3D | 9 | Stellt eine 3D-Balkendiagrammserie dar. |
| Bar3DStacked | 10 | Stellt eine 3D-gestapelte Balkendiagrammserie dar. |
| Bar3DPercentStacked | 11 | Stellt eine 3D zu 100% gestapelte Balkendiagrammserie dar. |
| Bubble | 12 | Stellt eine Blasendiagrammserie dar. |
| Bubble3D | 13 | Stellt eine 3D-Bubble-Diagrammreihe dar. |
| Spalte | 14 | Stellt eine Säulen-Diagrammreihe dar. |
| ColumnStacked | 15 | Stellt eine gestapelte Säulen-Diagrammreihe dar. |
| ColumnPercentStacked | 16 | Stellt eine zu 100 % gestapelte Säulen-Diagrammreihe dar. |
| Column3D | 17 | Stellt eine 3D-Säulen-Diagrammreihe dar. |
| Column3DStacked | 18 | Stellt eine 3D-gestapelte Säulen-Diagrammreihe dar. |
| Column3DPercentStacked | 19 | Stellt eine 3D zu 100 % gestapelte Säulen-Diagrammreihe dar. |
| Column3DClustered | 20 | Stellt eine 3D gruppierte Säulen-Diagrammreihe dar. |
| Donut | 21 | Stellt eine Donut-Diagrammreihe dar. |
| Linie | 22 | Stellt eine Linien-Diagrammreihe dar. |
| LineStacked | 23 | Stellt eine gestapelte Linien-Diagrammreihe dar. |
| LinePercentStacked | 24 | Stellt eine zu 100 % gestapelte Linien-Diagrammreihe dar. |
| Line3D | 25 | Stellt eine 3D-Linien-Diagrammreihe dar. |
| Pie | 26 | Stellt eine Kreisdiagrammreihe dar. |
| Pie3D | 27 | Stellt eine 3D-Kreisdiagrammreihe dar. |
| PieOfBar | 28 | Stellt eine Kreis-in-Balken-Diagrammreihe dar. |
| PieOfPie | 29 | Stellt eine Kreis-in-Kreis-Diagrammreihe dar. |
| Radar | 30 | Stellt eine Radar-Diagrammreihe dar. |
| Scatter | 31 | Stellt eine Streudiagrammreihe dar. |
| Aktie | 32 | Stellt eine Börsen-Diagrammreihe dar. |
| Oberfläche | 33 | Stellt eine Oberflächen-Diagrammreihe dar. |
| Surface3D | 34 | Stellt eine 3D-Oberflächen-Diagrammreihe dar. |
| Baumkarte | 35 | Stellt eine Baumkarten-Diagrammreihe dar. |
| Sonnenstrahl | 36 | Stellt eine Sonnenblüten-Diagrammreihe dar. |
| Histogramm | 37 | Stellt eine Histogramm-Diagrammreihe dar. |
| Pareto | 38 | Stellt eine Pareto-Diagrammserie dar. |
| ParetoLine | 39 | Stellt eine Pareto-Linien-Diagrammserie dar. |
| BoxAndWhisker | 40 | Stellt eine Box‑und‑Whisker-Diagrammserie dar. |
| Wasserfall | 41 | Stellt eine Wasserfall-Diagrammserie dar. |
| Trichter | 42 | Stellt eine Trichter‑Diagrammserie dar. |
| RegionMap | 43 | Stellt eine Region‑Karten‑Diagrammserie dar. |


## Beispiele



Zeigt, wie man eine bestimmte Diagrammserie entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Entfernt alle Serien des Spaltentyps.
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

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
