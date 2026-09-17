---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType méthode"
linktitle: "get_SeriesType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType méthode. Obtient le type de cette série de graphique en C++."
type: docs
weight: 11500
url: /fr/cpp/aspose.words.drawing.charts/chartseries/get_seriestype/
---
## ChartSeries::get_SeriesType method


Obtient le type de cette série de graphique.

```cpp
Aspose::Words::Drawing::Charts::ChartSeriesType Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType()
```


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

* Enum [ChartSeriesType](../../chartseriestype/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
