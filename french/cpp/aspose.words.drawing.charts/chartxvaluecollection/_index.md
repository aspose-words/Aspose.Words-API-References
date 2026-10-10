---
title: "Aspose::Words::Drawing::Charts::ChartXValueCollection class"
linktitle: "ChartXValueCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartXValueCollection class. Représente une collection de valeurs X pour une série de graphique en C++."
type: docs
weight: 18400
url: /fr/cpp/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class


Représente une collection de valeurs X pour une série de graphique.

```cpp
class ChartXValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Count](./get_count/)() | Obtient le nombre d'éléments dans cette collection. |
| [get_FormatCode](./get_formatcode/)() | Obtient ou définit le code de format appliqué aux valeurs X. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit la valeur X à l'indice spécifié. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Obtient ou définit la valeur X à l'indice spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Remarques


Tous les éléments de la collection, à l'exception de **null**, doivent avoir le même [ValueType](../chartxvalue/get_valuetype/).

La collection ne permet que de modifier les valeurs X. Pour ajouter ou insérer de nouvelles valeurs à une série de graphique, ou supprimer des valeurs, les méthodes appropriées de la classe [ChartSeries](../chartseries/) peuvent être utilisées.

## Exemples



Montre comment obtenir les données d'une série de graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // Efface le format individuel de tous les points de données.
    // Les points de données et les valeurs de données sont en correspondance un à un dans les graphiques en colonnes.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Obtenir la valeur Y.
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Modifier les couleurs des valeurs max et min.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
