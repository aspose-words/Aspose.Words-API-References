---
title: ChartXValue.FromDouble
linktitle: FromDouble
articleTitle: FromDouble
second_title: Aspose.Words för .NET
description: Upptäck ChartXValue FromDouble-metoden för att enkelt skapa ChartXValue-instanser av typen Double, vilket förbättrar dina datavisualiseringsmöjligheter.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartxvalue/fromdouble/
---
## ChartXValue.FromDouble method

Skapar en[`ChartXValue`](../) exempel påDouble typ.

```csharp
public static ChartXValue FromDouble(double value)
```

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

* class [ChartXValue](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
