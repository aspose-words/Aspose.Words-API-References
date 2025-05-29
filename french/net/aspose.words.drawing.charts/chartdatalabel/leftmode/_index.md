---
title: ChartDataLabel.LeftMode
linktitle: LeftMode
articleTitle: LeftMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartDataLabel LeftMode pour personnaliser le positionnement des étiquettes de données dans vos graphiques. Améliorez la clarté et la présentation grâce à un contrôle précis.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chartdatalabel/leftmode/
---
## ChartDataLabel.LeftMode property

Obtient ou définit le mode d'interprétation du[`Left`](../left/) valeur de la propriété : si elle définit l'emplacement de l'étiquette de données à partir du bord gauche du graphique ou à partir de la position spécifiée par son[`Position`](../position/) Propriété .

```csharp
public ChartDataLabelLocationMode LeftMode { get; set; }
```

## Remarques

La propriété ne peut pas être définie dans un graphique Word 2016.

## Exemples

Montre comment placer les étiquettes de données du graphique en anneau en dehors de l'anneau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Supprimer la série générée par défaut.
seriesColl.Clear();

// Masquer la légende.
chart.Legend.Position = LegendPosition.None;

// Générer des données.
const int dataLength = 20;
double totalValue = 0;
string[] categories = new string[dataLength];
double[] values = new double[dataLength];

for (int i = 0; i < dataLength; i++)
{
    categories[i] = $"Category {i}";
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

ChartSeries series = seriesColl.Add("Series 1", categories, values);
series.HasDataLabels = true;

ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.ShowLeaderLines = true;

// La propriété Position ne peut pas être utilisée pour les graphiques en anneau. Placer les étiquettes de données à l'aide des propriétés Gauche et Haut
// propriétés autour d'un cercle en dehors du graphique en anneau.
// L'origine se trouve dans le coin supérieur gauche du graphique.

const double titleAreaHeight = 25.5; // Cela peut être calculé en utilisant le texte du titre et la police.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Ceci peut être calculé en utilisant la police de l'étiquette.
const double oneCharLabelWidth = 12.75; // Cela peut être calculé pour chaque étiquette en utilisant son texte et sa police.
const double twoCharLabelWidth = 17.25; // Cela peut être calculé pour chaque étiquette en utilisant son texte et sa police.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Étant donné que les points de données commencent en haut, les coordonnées X utilisées dans les propriétés Left et Top de
// les étiquettes de données pointent vers la droite et les coordonnées Y pointent vers le bas, l'angle de départ est -PI/2.
double totalAngle = -System.Math.PI / 2;
ChartDataLabel previousLabel = null;

for (int i = 0; i < series.YValues.Count; i++)
{
    ChartDataLabel dataLabel = dataLabels[i];

    double value = series.YValues[i].DoubleValue;
    double labelWidth;
    if (value < 10)
        labelWidth = oneCharLabelWidth;
    else
        labelWidth = twoCharLabelWidth;
    double labelSegmentAngle = value / totalValue * 2 * System.Math.PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System.Math.Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System.Math.Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // Si l'étiquette de données actuelle chevauche d'autres étiquettes, déplacez-la horizontalement.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Déplacez-vous vers la droite en haut, vers la gauche en bas.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System.Math.PI);
        int factor;
        if (isOnTop)
            factor = 1;
        else
            factor = -1;

        labelLeft = previousLabel.Left + labelWidth * factor + labelMargin;
    }

    dataLabel.Left = labelLeft;
    dataLabel.LeftMode = ChartDataLabelLocationMode.Absolute;
    dataLabel.Top = labelTop;
    dataLabel.TopMode = ChartDataLabelLocationMode.Absolute;

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc.Save(ArtifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### Voir également

* enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* class [ChartDataLabel](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
