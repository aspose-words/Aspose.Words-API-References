---
title: Add
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 30
url: /net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(string, string[], double[]) {1}

Adds new [`ChartSeries`](../../chartseries) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Return Value

Recently added [`ChartSeries`](../../chartseries) object.

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // There are several ways of populating a chart's series collection.
    // Different series schemas are intended for different chart types.
    // 1 -  Column chart with columns grouped and banded along the X-axis by category:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insert two series of decimal values containing a value for each respective category.
    // This column chart will have three groups, each with two columns.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 -  Area chart with dates distributed along the X-axis:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insert a series with a decimal value for each respective date.
    // The dates will be distributed along a linear X-axis,
    // and the values added to this series will create data points.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 -  2D scatter plot:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Each series will need two decimal arrays of equal length.
    // The first array contains X-values, and the second contains corresponding Y-values
    // of data points on the chart's graph.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 -  Bubble chart:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Each series will need three decimal arrays of equal length.
    // The first array contains X-values, the second contains corresponding Y-values,
    // and the third contains diameters for each of the graph's data points.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();

    return chart;
}
```

### See Also

* class [ChartSeries](../../chartseries)
* class [ChartSeriesCollection](../../chartseriescollection)
* namespace [Aspose.Words.Drawing.Charts](../../chartseriescollection)
* assembly [Aspose.Words](../../../)

---

## Add(string, double[], double[]) {2}

Adds new [`ChartSeries`](../../chartseries) to this collection. Use this method to add series to any type of Scatter charts.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Return Value

Recently added [`ChartSeries`](../../chartseries) object.

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // There are several ways of populating a chart's series collection.
    // Different series schemas are intended for different chart types.
    // 1 -  Column chart with columns grouped and banded along the X-axis by category:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insert two series of decimal values containing a value for each respective category.
    // This column chart will have three groups, each with two columns.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 -  Area chart with dates distributed along the X-axis:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insert a series with a decimal value for each respective date.
    // The dates will be distributed along a linear X-axis,
    // and the values added to this series will create data points.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 -  2D scatter plot:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Each series will need two decimal arrays of equal length.
    // The first array contains X-values, and the second contains corresponding Y-values
    // of data points on the chart's graph.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 -  Bubble chart:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Each series will need three decimal arrays of equal length.
    // The first array contains X-values, the second contains corresponding Y-values,
    // and the third contains diameters for each of the graph's data points.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();

    return chart;
}
```

### See Also

* class [ChartSeries](../../chartseries)
* class [ChartSeriesCollection](../../chartseriescollection)
* namespace [Aspose.Words.Drawing.Charts](../../chartseriescollection)
* assembly [Aspose.Words](../../../)

---

## Add(string, DateTime[], double[]) {3}

Adds new [`ChartSeries`](../../chartseries) to this collection. Use this method to add series to any type of Area, Radar and Stock charts.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // There are several ways of populating a chart's series collection.
    // Different series schemas are intended for different chart types.
    // 1 -  Column chart with columns grouped and banded along the X-axis by category:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insert two series of decimal values containing a value for each respective category.
    // This column chart will have three groups, each with two columns.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 -  Area chart with dates distributed along the X-axis:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insert a series with a decimal value for each respective date.
    // The dates will be distributed along a linear X-axis,
    // and the values added to this series will create data points.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 -  2D scatter plot:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Each series will need two decimal arrays of equal length.
    // The first array contains X-values, and the second contains corresponding Y-values
    // of data points on the chart's graph.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 -  Bubble chart:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Each series will need three decimal arrays of equal length.
    // The first array contains X-values, the second contains corresponding Y-values,
    // and the third contains diameters for each of the graph's data points.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();

    return chart;
}
```

### See Also

* class [ChartSeries](../../chartseries)
* class [ChartSeriesCollection](../../chartseriescollection)
* namespace [Aspose.Words.Drawing.Charts](../../chartseriescollection)
* assembly [Aspose.Words](../../../)

---

## Add(string, double[], double[], double[]) {4}

Adds new [`ChartSeries`](../../chartseries) to this collection. Use this method to add series to any type of Bubble charts.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Return Value

Recently added [`ChartSeries`](../../chartseries) object.

### Examples

Shows how to create an appropriate type of chart series for a graph type.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // There are several ways of populating a chart's series collection.
    // Different series schemas are intended for different chart types.
    // 1 -  Column chart with columns grouped and banded along the X-axis by category:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insert two series of decimal values containing a value for each respective category.
    // This column chart will have three groups, each with two columns.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 -  Area chart with dates distributed along the X-axis:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insert a series with a decimal value for each respective date.
    // The dates will be distributed along a linear X-axis,
    // and the values added to this series will create data points.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 -  2D scatter plot:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Each series will need two decimal arrays of equal length.
    // The first array contains X-values, and the second contains corresponding Y-values
    // of data points on the chart's graph.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 -  Bubble chart:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Each series will need three decimal arrays of equal length.
    // The first array contains X-values, the second contains corresponding Y-values,
    // and the third contains diameters for each of the graph's data points.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();

    return chart;
}
```

### See Also

* class [ChartSeries](../../chartseries)
* class [ChartSeriesCollection](../../chartseriescollection)
* namespace [Aspose.Words.Drawing.Charts](../../chartseriescollection)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
