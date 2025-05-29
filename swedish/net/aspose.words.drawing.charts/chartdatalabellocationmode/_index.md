---
title: ChartDataLabelLocationMode Enum
linktitle: ChartDataLabelLocationMode
articleTitle: ChartDataLabelLocationMode
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.ChartDataLabelLocationMode för att effektivt anpassa positioneringen av dataetiketter med intuitiva inställningar för egenskaperna Vänster och Överst.
type: docs
weight: 950
url: /sv/net/aspose.words.drawing.charts/chartdatalabellocationmode/
---
## ChartDataLabelLocationMode enumeration

Anger hur värdena som anger platsen för en dataetikett - den[`Left`](../chartdatalabel/left/) och [`Top`](../chartdatalabel/top/) egenskaper - tolkas.

```csharp
public enum ChartDataLabelLocationMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Offset | `0` | Platsen för en dataetikett anges av en förskjutning från positionen definierad av dess [`Position`](../chartdatalabel/position/) egendom. |
| Absolute | `1` | Platsen för en dataetikett anges med absoluta koordinater, med början från det övre vänstra hörnet i ett diagram. |

## Exempel

Visar hur man placerar dataetiketter från ringdiagrammet utanför ringdiagrammet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Radera standardgenererad serie.
seriesColl.Clear();

// Dölj förklaringen.
chart.Legend.Position = LegendPosition.None;

// Generera data.
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

// Egenskapen Position kan inte användas för ringdiagram. Nu placerar vi dataetiketter med hjälp av vänster- och övre fältet.
// egenskaper runt en cirkel utanför diagrammets ring.
// Origon finns i diagrammets övre vänstra hörn.

const double titleAreaHeight = 25.5; // Detta kan beräknas med hjälp av titeltext och teckensnitt.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Detta kan beräknas med hjälp av etikettfont.
const double oneCharLabelWidth = 12.75; // Detta kan beräknas för varje etikett med hjälp av dess text och typsnitt.
const double twoCharLabelWidth = 17.25; // Detta kan beräknas för varje etikett med hjälp av dess text och typsnitt.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Eftersom datapunkterna börjar högst upp, används X-koordinaterna i egenskaperna Vänster och Överst för
// dataetiketterna pekar åt höger och Y-koordinaterna pekar nedåt, startvinkeln är -PI/2.
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

    // Om den aktuella dataetiketten överlappar andra etiketter, flytta den horisontellt.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Flytta åt höger upptill, åt vänster nedtill.
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

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
