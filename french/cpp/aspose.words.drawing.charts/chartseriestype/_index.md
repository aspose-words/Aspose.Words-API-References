---
title: "Aspose::Words::Drawing::Charts::ChartSeriesType énumération"
linktitle: "ChartSeriesType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesType enum. Spécifie un type de série de graphique en C++."
type: docs
weight: 27500
url: /fr/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Spécifie un type de série de graphique.

```cpp
enum class ChartSeriesType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Area | 0 | Représente une série de graphique en aires. |
| AreaStacked | 1 | Représente une série de graphique en aires empilées. |
| AreaPercentStacked | 2 | Représente une série de graphique en aires empilées à 100 %. |
| Area3D | 3 | Représente une série de graphique en aires 3D. |
| Area3DStacked | 4 | Représente une série de graphique en aires empilées 3D. |
| Area3DPercentStacked | 5 | Représente une série de graphique en aires empilées à 100 % 3D. |
| Bar | 6 | Représente une série de graphique à barres. |
| BarStacked | 7 | Représente une série de graphique à barres empilées. |
| BarPercentStacked | 8 | Représente une série de graphique à barres empilées à 100 %. |
| Bar3D | 9 | Représente une série de graphique à barres 3D. |
| Bar3DStacked | 10 | Représente une série de graphique à barres empilées 3D. |
| Bar3DPercentStacked | 11 | Représente une série de diagramme à barres empilées à 100 % en 3D. |
| Bubble | 12 | Représente une série de diagramme à bulles. |
| Bubble3D | 13 | Représente une série de diagramme à bulles en 3D. |
| Colonne | 14 | Représente une série de diagramme à colonnes. |
| ColumnStacked | 15 | Représente une série de diagramme à colonnes empilées. |
| ColumnPercentStacked | 16 | Représente une série de diagramme à colonnes empilées à 100 %. |
| Column3D | 17 | Représente une série de diagramme à colonnes en 3D. |
| Column3DStacked | 18 | Représente une série de diagramme à colonnes empilées en 3D. |
| Column3DPercentStacked | 19 | Représente une série de diagramme à colonnes empilées à 100 % en 3D. |
| Column3DClustered | 20 | Représente une série de diagramme à colonnes groupées en 3D. |
| Doughnut | 21 | Représente une série de diagramme en anneau. |
| Ligne | 22 | Représente une série de diagramme en ligne. |
| LineStacked | 23 | Représente une série de diagramme en ligne empilée. |
| LinePercentStacked | 24 | Représente une série de diagramme en ligne empilée à 100 %. |
| Line3D | 25 | Représente une série de diagramme en ligne en 3D. |
| Camembert | 26 | Représente une série de diagramme circulaire. |
| Pie3D | 27 | Représente une série de diagramme circulaire en 3D. |
| PieOfBar | 28 | Représente une série de diagramme en anneau de barres. |
| PieOfPie | 29 | Représente une série de diagramme en anneau d'anneau. |
| Radar | 30 | Représente une série de diagramme radar. |
| Nuage de points | 31 | Représente une série de diagramme de dispersion. |
| Bourse | 32 | Représente une série de diagramme boursier. |
| Surface | 33 | Représente une série de diagramme de surface. |
| Surface3D | 34 | Représente une série de diagramme de surface en 3D. |
| Carte à arbres | 35 | Représente une série de diagramme en carte arborescente. |
| Diagramme en rayons | 36 | Représente une série de graphique Sunburst. |
| Histogramme | 37 | Représente une série de graphique Histogramme. |
| Pareto | 38 | Représente une série de graphique Pareto. |
| ParetoLine | 39 | Représente une série de graphique Pareto Line. |
| Boîte et moustaches | 40 | Représente une série de graphique Boîte à moustaches. |
| Cascade | 41 | Représente une série de graphique en cascade. |
| Funnel | 42 | Représente une série de graphique en entonnoir. |
| RegionMap | 43 | Représente une série de graphique Carte régionale. |


## Exemples



Montre comment supprimer une série de graphique spécifique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Supprime toutes les séries de type Colonne.
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

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
