---
title: Class ChartYValueCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartYValueCollection klass. Representerar en samling Yvärden för en diagramserie.
type: docs
weight: 880
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
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Hämtar antalet föremål i den här samlingen. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Hämtar eller ställer in Y-värdet på det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Returnerar ett uppräkningsobjekt. |

### Anmärkningar

Alla föremål i samlingen förutom **null** måste ha samma[`ValueType`](../chartyvalue/valuetype/).

Samlingen tillåter endast att ändra Y-värden. För att lägga till eller infoga nya värden i en diagramserie, eller ta bort värden, lämpliga metoder för[`ChartSeries`](../chartseries/) klass kan användas.

### Exempel

Visar hur man får diagramseriedata.

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
    // Datapunkter och datavärden är en-till-en i kolumndiagram.
    series.DataPoints[i].ClearFormat();

    // Få Y-värde.
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

// Ändra färger på max- och minvärden.
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


