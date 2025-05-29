---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartYValueCollection, din lösning för att effektivt hantera Y-värden i diagramserier.
type: docs
weight: 1200
url: /sv/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

Representerar en samling Y-värden för en diagramserie.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Hämtar antalet objekt i den här samlingen. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | Hämtar eller ställer in formatkoden som tillämpas på Y-värdena. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Hämtar eller ställer in Y-värdet vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |

## Anmärkningar

Alla föremål i samlingen förutom**null** måste ha samma[`ValueType`](../chartyvalue/valuetype/).

Samlingen tillåter endast ändring av Y-värden. För att lägga till eller infoga nya värden i en diagramserie, eller ta bort värden, använder du lämpliga metoder för[`ChartSeries`](../chartseries/) klass kan användas.

## Exempel

Visar hur man hämtar data från diagramserier.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Rensa individuellt format för alla datapunkter.
    // Datapunkter och datavärden är ett-till-ett i kolumndiagram.
    series.DataPoints[i].ClearFormat();

    // Hämta Y-värde.
    double yValue = series.YValues[i].DoubleValue;

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

// Ändra färgerna på max- och min-värdena.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Se även

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
