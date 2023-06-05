---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: ChartSeries Add method. Adds the specified X value to the chart series. If the series supports Y values and bubble sizes they will be empty for the X value in C#.
type: docs
weight: 160
url: /net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value.

```csharp
public void Add(ChartXValue xValue)
```

### See Also

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartseries/)
* assembly [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Adds the specified X and Y values to the chart series.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
```

## Examples

Shows how to add/remove chart data values.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Remove the first value in the both series.
department1Series.Remove(0);
department2Series.Remove(0);

// Add new values to the both series.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

Shows how to populate chart series with data.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Clear X and Y values of the first series.
series1.ClearValues();

// Populate the series with data.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// Clear X and Y values of the second series.
series2.ClearValues();

// Populate the series with data.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### See Also

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartseries/)
* assembly [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Adds the specified X value, Y value and bubble size to the chart series.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

### See Also

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartseries/)
* assembly [Aspose.Words](../../../)
