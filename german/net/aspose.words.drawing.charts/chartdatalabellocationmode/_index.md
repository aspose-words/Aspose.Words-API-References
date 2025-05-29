---
title: ChartDataLabelLocationMode Enum
linktitle: ChartDataLabelLocationMode
articleTitle: ChartDataLabelLocationMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.ChartDataLabelLocationMode, um die Positionierung von Datenbeschriftungen mit intuitiven Eigenschafteneinstellungen für „Links“ und „Oben“ effektiv anzupassen.
type: docs
weight: 950
url: /de/net/aspose.words.drawing.charts/chartdatalabellocationmode/
---
## ChartDataLabelLocationMode enumeration

Gibt an, wie die Werte, die den Speicherort eines Datenlabels angeben - die[`Left`](../chartdatalabel/left/) und [`Top`](../chartdatalabel/top/) Eigenschaften - werden interpretiert.

```csharp
public enum ChartDataLabelLocationMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Offset | `0` | Die Position eines Datenlabels wird durch einen Offset von der durch sein definierten Position angegeben.[`Position`](../chartdatalabel/position/) Eigenschaft. |
| Absolute | `1` | Die Position einer Datenbeschriftung wird mithilfe absoluter Koordinaten angegeben, ausgehend von der oberen linken Ecke eines Diagramms. |

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
