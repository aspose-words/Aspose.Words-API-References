---
title: "Aspose::Words::Drawing::Charts::ChartSeriesType enum"
linktitle: "ChartSeriesType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesType enum. Specifica un tipo di serie di grafico in C++."
type: docs
weight: 27500
url: /it/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Specifica un tipo di serie di grafico.

```cpp
enum class ChartSeriesType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Area | 0 | Rappresenta una serie di grafico a area. |
| AreaStacked | 1 | Rappresenta una serie di grafico a area impilata. |
| AreaPercentStacked | 2 | Rappresenta una serie di grafico a area impilata al 100%. |
| Area3D | 3 | Rappresenta una serie di grafico a area 3D. |
| Area3DStacked | 4 | Rappresenta una serie di grafico a area impilata 3D. |
| Area3DPercentStacked | 5 | Rappresenta una serie di grafico a area impilata 3D al 100%. |
| Barra | 6 | Rappresenta una serie di grafico a barre. |
| BarStacked | 7 | Rappresenta una serie di grafico a barre impilata. |
| BarPercentStacked | 8 | Rappresenta una serie di grafico a barre impilata al 100%. |
| Bar3D | 9 | Rappresenta una serie di grafico a barre 3D. |
| Bar3DStacked | 10 | Rappresenta una serie di grafico a barre impilata 3D. |
| Bar3DPercentStacked | 11 | Rappresenta una serie di grafico a barre impilate al 100% 3D. |
| Bubble | 12 | Rappresenta una serie di grafico a bolle. |
| Bubble3D | 13 | Rappresenta una serie di grafico a bolle 3D. |
| Colonna | 14 | Rappresenta una serie di grafico a colonne. |
| ColumnStacked | 15 | Rappresenta una serie di grafico a colonne impilate. |
| ColumnPercentStacked | 16 | Rappresenta una serie di grafico a colonne impilate al 100%. |
| Column3D | 17 | Rappresenta una serie di grafico a colonne 3D. |
| Column3DStacked | 18 | Rappresenta una serie di grafico a colonne impilate 3D. |
| Column3DPercentStacked | 19 | Rappresenta una serie di grafico a colonne impilate al 100% 3D. |
| Column3DClustered | 20 | Rappresenta una serie di grafico a colonne raggruppate 3D. |
| Doughnut | 21 | Rappresenta una serie di grafico a ciambella. |
| Linea | 22 | Rappresenta una serie di grafico a linee. |
| LineStacked | 23 | Rappresenta una serie di grafico a linee impilate. |
| LinePercentStacked | 24 | Rappresenta una serie di grafico a linee impilate al 100%. |
| Line3D | 25 | Rappresenta una serie di grafico a linee 3D. |
| Torta | 26 | Rappresenta una serie di grafico a torta. |
| Pie3D | 27 | Rappresenta una serie di grafico a torta 3D. |
| PieOfBar | 28 | Rappresenta una serie di grafico a torta di barre. |
| PieOfPie | 29 | Rappresenta una serie di grafico a torta di torta. |
| Radar | 30 | Rappresenta una serie di grafico radar. |
| Dispersione | 31 | Rappresenta una serie di grafico a dispersione. |
| Azioni | 32 | Rappresenta una serie di grafico azionario. |
| Superficie | 33 | Rappresenta una serie di grafico di superficie. |
| Superficie3D | 34 | Rappresenta una serie di grafico di superficie 3D. |
| Mappa ad albero | 35 | Rappresenta una serie di grafico ad albero. |
| Raggiera | 36 | Rappresenta una serie di grafico Sunburst. |
| Istogramma | 37 | Rappresenta una serie di grafico Istogramma. |
| Pareto | 38 | Rappresenta una serie di grafico Pareto. |
| ParetoLine | 39 | Rappresenta una serie di grafico Pareto Line. |
| BoxAndWhisker | 40 | Rappresenta una serie di grafico Box and Whisker. |
| Cascata | 41 | Rappresenta una serie di grafico Waterfall. |
| Imbuto | 42 | Rappresenta una serie di grafico Funnel. |
| RegionMap | 43 | Rappresenta una serie di grafico Region Map. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
