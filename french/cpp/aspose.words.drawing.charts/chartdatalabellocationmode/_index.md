---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode enum"
linktitle: "ChartDataLabelLocationMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode enum. Spécifie comment les valeurs qui indiquent l'emplacement d'une étiquette de données - les propriétés Left et Top - sont interprétées en C++."
type: docs
weight: 27167
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabellocationmode/
---
## ChartDataLabelLocationMode enum


Spécifie comment les valeurs qui indiquent l'emplacement d'une étiquette de données - les propriétés [Left](../chartdatalabel/get_left/) et [Top](../chartdatalabel/get_top/) - sont interprétées.

```cpp
enum class ChartDataLabelLocationMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Offset | 0 | L'emplacement d'une étiquette de données est spécifié par un décalage par rapport à la position définie par sa propriété [Position](../chartdatalabel/get_position/). |
| Absolu | 1 | L'emplacement d'une étiquette de données est spécifié en utilisant des coordonnées absolues, en partant du coin supérieur gauche d'un graphique. |


## Exemples



Montre comment placer les étiquettes de données d'un graphique en anneau à l'extérieur de l'anneau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Supprimer la série générée par défaut.
seriesColl->Clear();

// Masquer la légende.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Générer des données.
const int32_t dataLength = 20;
double totalValue = 0;
auto categories = System::MakeArray<System::String>(dataLength);
auto values = System::MakeArray<double>(dataLength, 0);

for (int32_t i = 0; i < dataLength; i++)
{
    categories[i] = System::String::Format(u"Category {0}", i);
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", categories, values);
series->set_HasDataLabels(true);

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->set_ShowLeaderLines(true);

// La propriété Position ne peut pas être utilisée pour les graphiques en anneau. Plaçons les étiquettes de données en utilisant les propriétés Left et Top
// propriétés autour d'un cercle à l'extérieur de l'anneau du graphique.
// L'origine se trouve dans le coin supérieur gauche du graphique.

const double titleAreaHeight = 25.5;
// Cela peut être calculé en utilisant le texte du titre et la police.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Cela peut être calculé en utilisant la police de l'étiquette.
const double oneCharLabelWidth = 12.75;
// Cela peut être calculé pour chaque étiquette en utilisant son texte et sa police.
const double twoCharLabelWidth = 17.25;
// Cela peut être calculé pour chaque étiquette en utilisant son texte et sa police.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Parce que les points de données commencent en haut, les coordonnées X utilisées dans les propriétés Left et Top de
// les étiquettes de données pointent vers la droite et les coordonnées Y pointent vers le bas, l'angle de départ est -PI/2.
double totalAngle = -System::Math::PI / 2;
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> previousLabel;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> dataLabel = dataLabels->idx_get(i);

    double value = series->get_YValues()->idx_get(i)->get_DoubleValue();
    double labelWidth;
    if (value < 10)
    {
        labelWidth = oneCharLabelWidth;
    }
    else
    {
        labelWidth = twoCharLabelWidth;
    }
    double labelSegmentAngle = value / totalValue * 2 * System::Math::PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System::Math::Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System::Math::Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // Si l'étiquette de données actuelle chevauche d'autres étiquettes, déplacez‑la horizontalement.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Déplacez‑vous vers la droite en haut, vers la gauche en bas.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System::Math::PI);
        int32_t factor;
        if (isOnTop)
        {
            factor = 1;
        }
        else
        {
            factor = -1;
        }

        labelLeft = previousLabel->get_Left() + labelWidth * factor + labelMargin;
    }

    dataLabel->set_Left(labelLeft);
    dataLabel->set_LeftMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);
    dataLabel->set_Top(labelTop);
    dataLabel->set_TopMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChartLabelPosition.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
