---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartXValue, din lösning för att definiera X-värden i diagramserier och förbättra datavisualiseringen utan ansträngning.
type: docs
weight: 1160
url: /sv/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Representerar ett X-värde för en diagramserie.

```csharp
public class ChartXValue
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Hämtar det lagrade datum- och tidsvärdet. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Hämtar det lagrade numeriska värdet. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Hämtar det lagrade flernivåvärdet. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Hämtar det lagrade strängvärdet. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Hämtar det lagrade tidsvärdet. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Hämtar typen av X-värdet som lagras i objektet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Skapar en`ChartXValue` exempel påDateTime typ. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Skapar en`ChartXValue` exempel påDouble typ. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Skapar en`ChartXValue` exempel påMultilevel typ. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Skapar en`ChartXValue` exempel påString typ. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Skapar en`ChartXValue` exempel påTime typ. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Hämtar en flagga som anger om det angivna objektet är lika med det aktuella X-värdeobjektet. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Hämtar en hashkod för det aktuella X-värdeobjektet. |

## Anmärkningar

Den här klassen innehåller ett antal statiska metoder för att skapa ett X-värde av en viss typ. The [`ValueType`](./valuetype/) Med egenskapen kan du bestämma typen av ett befintligt X-värde.

Alla X-värden som inte är null i en diagramserie måste vara av samma värde.[`ChartXValueType`](../chartxvaluetype/) typ.

## Exempel

Visar hur man fyller diagramserier med data.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Rensa X- och Y-värdena för den första serien.
series1.ClearValues();

// Fyll serien med data.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Rensa X- och Y-värdena för den andra serien.
series2.Clear();

// Fyll serien med data.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
