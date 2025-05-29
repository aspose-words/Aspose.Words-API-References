---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
articleTitle: ChartXValueCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartXValueCollection, din lösning för att effektivt hantera X-värdesamlingar i diagramserier.
type: docs
weight: 1170
url: /sv/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Representerar en samling av X-värden för en diagramserie.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Hämtar antalet objekt i den här samlingen. |
| [FormatCode](../../aspose.words.drawing.charts/chartxvaluecollection/formatcode/) { get; set; } | Hämtar eller ställer in formatkoden som tillämpas på X-värdena. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Hämtar eller ställer in X-värdet vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |

## Anmärkningar

Alla föremål i samlingen förutom**null** måste ha samma[`ValueType`](../chartxvalue/valuetype/).

Samlingen tillåter endast ändring av X-värden. För att lägga till eller infoga nya värden i en diagramserie, eller ta bort värden, använd lämpliga metoder för[`ChartSeries`](../chartseries/) klass kan användas.

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
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
