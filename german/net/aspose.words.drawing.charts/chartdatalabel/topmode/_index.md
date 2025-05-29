---
title: ChartDataLabel.TopMode
linktitle: TopMode
articleTitle: TopMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die TopMode-Eigenschaft von ChartDataLabel, um die Positionierung von Datenbeschriftungen in Ihren Diagrammen anzupassen. Verbessern Sie Klarheit und Präzision in Ihren visuellen Datenpräsentationen!
type: docs
weight: 220
url: /de/net/aspose.words.drawing.charts/chartdatalabel/topmode/
---
## ChartDataLabel.TopMode property

Ermittelt oder setzt den Interpretationsmodus des[`Top`](../top/) Eigenschaftswert: ob die Position der Datenbeschriftung vom oberen Rand des Diagramms oder von der durch seine angegebene Position festgelegt wird[`Position`](../position/) Eigenschaft.

```csharp
public ChartDataLabelLocationMode TopMode { get; set; }
```

## Bemerkungen

Die Eigenschaft kann in einem Word 2016-Diagramm nicht festgelegt werden.

## Beispiele

Zeigt, wie Datenbeschriftungen eines Ringdiagramms außerhalb des Rings platziert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

// Legende ausblenden.
chart.Legend.Position = LegendPosition.None;

// Daten generieren.
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

// Die Eigenschaft Position kann nicht für Ringdiagramme verwendet werden. Platzieren wir Datenbeschriftungen mit den Eigenschaften Left und Top
// Eigenschaften um einen Kreis außerhalb des Diagramm-Rings.
// Der Ursprung liegt in der oberen linken Ecke des Diagramms.

const double titleAreaHeight = 25.5; // Dies kann anhand des Titeltextes und der Schriftart berechnet werden.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Dies kann anhand der Beschriftungsschriftart berechnet werden.
const double oneCharLabelWidth = 12.75; // Dies kann für jedes Etikett anhand seines Textes und seiner Schriftart berechnet werden.
const double twoCharLabelWidth = 17.25; // Dies kann für jedes Etikett anhand seines Textes und seiner Schriftart berechnet werden.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Da die Datenpunkte oben beginnen, werden die X-Koordinaten in den Eigenschaften Left und Top von
// die Datenbeschriftungen zeigen nach rechts und die Y-Koordinaten nach unten, der Startwinkel beträgt -PI/2.
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

    // Wenn die aktuelle Datenbeschriftung andere Beschriftungen überlappt, verschieben Sie sie horizontal.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Oben nach rechts und unten nach links bewegen.
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

### Siehe auch

* enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* class [ChartDataLabel](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
