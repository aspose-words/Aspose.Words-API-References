---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: ChartSeriesCollection Add metod. Lägger till nyttChartSeries till denna samling. Använd den här metoden för att lägga till serier till alla typer av stapel kolumn linje och ytdiagram i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_3}

Lägger till nytt[`ChartSeries`](../../chartseries/) till denna samling. Använd den här metoden för att lägga till serier till alla typer av stapel-, kolumn-, linje- och ytdiagram.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Returvärde

Nyligen tillagd[`ChartSeries`](../../chartseries/) objekt.

## Exempel

Visar hur man skapar en lämplig typ av diagramserie för en graftyp.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Det finns flera sätt att fylla i ett diagrams seriesamling.
    // Olika seriescheman är avsedda för olika diagramtyper.
    // 1 - Kolumndiagram med kolumner grupperade och bandade längs X-axeln efter kategori:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Infoga två serier av decimalvärden som innehåller ett värde för varje respektive kategori.
    // Detta kolumndiagram kommer att ha tre grupper, var och en med två kolumner.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategorier är fördelade längs X-axeln, och värden är fördelade längs Y-axeln.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Ytdiagram med datum fördelade längs X-axeln:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Infoga en serie med ett decimalvärde för respektive datum.
    // Datumen kommer att fördelas längs en linjär X-axel,
    // och värdena som läggs till i denna serie kommer att skapa datapunkter.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D spridningsdiagram:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Varje serie kommer att behöva två decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden och den andra innehåller motsvarande Y-värden
    // av datapunkter på diagrammets graf.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Bubbeldiagram:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Varje serie kommer att behöva tre decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden, den andra innehåller motsvarande Y-värden,
    // och den tredje innehåller diametrar för var och en av grafens datapunkter.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Infoga ett diagram med hjälp av en dokumentbyggare med en specificerad diagramtyp, bredd och höjd, och ta bort dess demodata.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Se även

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add}

Lägger till nytt[`ChartSeries`](../../chartseries/) till denna samling. Använd den här metoden för att lägga till serier till alla typer av punktdiagram.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Returvärde

Nyligen tillagd[`ChartSeries`](../../chartseries/) objekt.

## Exempel

Visar hur man skapar en lämplig typ av diagramserie för en graftyp.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Det finns flera sätt att fylla i ett diagrams seriesamling.
    // Olika seriescheman är avsedda för olika diagramtyper.
    // 1 - Kolumndiagram med kolumner grupperade och bandade längs X-axeln efter kategori:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Infoga två serier av decimalvärden som innehåller ett värde för varje respektive kategori.
    // Detta kolumndiagram kommer att ha tre grupper, var och en med två kolumner.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategorier är fördelade längs X-axeln, och värden är fördelade längs Y-axeln.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Ytdiagram med datum fördelade längs X-axeln:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Infoga en serie med ett decimalvärde för respektive datum.
    // Datumen kommer att fördelas längs en linjär X-axel,
    // och värdena som läggs till i denna serie kommer att skapa datapunkter.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D spridningsdiagram:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Varje serie kommer att behöva två decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden och den andra innehåller motsvarande Y-värden
    // av datapunkter på diagrammets graf.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Bubbeldiagram:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Varje serie kommer att behöva tre decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden, den andra innehåller motsvarande Y-värden,
    // och den tredje innehåller diametrar för var och en av grafens datapunkter.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Infoga ett diagram med hjälp av en dokumentbyggare med en specificerad diagramtyp, bredd och höjd, och ta bort dess demodata.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Se även

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_2}

Lägger till nytt[`ChartSeries`](../../chartseries/) till denna samling. Använd den här metoden för att lägga till serier till alla typer av områdes-, radar- och aktiediagram.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

## Exempel

Visar hur man skapar en lämplig typ av diagramserie för en graftyp.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Det finns flera sätt att fylla i ett diagrams seriesamling.
    // Olika seriescheman är avsedda för olika diagramtyper.
    // 1 - Kolumndiagram med kolumner grupperade och bandade längs X-axeln efter kategori:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Infoga två serier av decimalvärden som innehåller ett värde för varje respektive kategori.
    // Detta kolumndiagram kommer att ha tre grupper, var och en med två kolumner.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategorier är fördelade längs X-axeln, och värden är fördelade längs Y-axeln.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Ytdiagram med datum fördelade längs X-axeln:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Infoga en serie med ett decimalvärde för respektive datum.
    // Datumen kommer att fördelas längs en linjär X-axel,
    // och värdena som läggs till i denna serie kommer att skapa datapunkter.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D spridningsdiagram:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Varje serie kommer att behöva två decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden och den andra innehåller motsvarande Y-värden
    // av datapunkter på diagrammets graf.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Bubbeldiagram:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Varje serie kommer att behöva tre decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden, den andra innehåller motsvarande Y-värden,
    // och den tredje innehåller diametrar för var och en av grafens datapunkter.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Infoga ett diagram med hjälp av en dokumentbyggare med en specificerad diagramtyp, bredd och höjd, och ta bort dess demodata.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Se även

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_1}

Lägger till nytt[`ChartSeries`](../../chartseries/)till denna samling. Använd den här metoden för att lägga till serier till alla typer av bubbeldiagram.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Returvärde

Nyligen tillagd[`ChartSeries`](../../chartseries/) objekt.

## Exempel

Visar hur man skapar en lämplig typ av diagramserie för en graftyp.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Det finns flera sätt att fylla i ett diagrams seriesamling.
    // Olika seriescheman är avsedda för olika diagramtyper.
    // 1 - Kolumndiagram med kolumner grupperade och bandade längs X-axeln efter kategori:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Infoga två serier av decimalvärden som innehåller ett värde för varje respektive kategori.
    // Detta kolumndiagram kommer att ha tre grupper, var och en med två kolumner.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategorier är fördelade längs X-axeln, och värden är fördelade längs Y-axeln.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Ytdiagram med datum fördelade längs X-axeln:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Infoga en serie med ett decimalvärde för respektive datum.
    // Datumen kommer att fördelas längs en linjär X-axel,
    // och värdena som läggs till i denna serie kommer att skapa datapunkter.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D spridningsdiagram:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Varje serie kommer att behöva två decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden och den andra innehåller motsvarande Y-värden
    // av datapunkter på diagrammets graf.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Bubbeldiagram:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Varje serie kommer att behöva tre decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden, den andra innehåller motsvarande Y-värden,
    // och den tredje innehåller diametrar för var och en av grafens datapunkter.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Infoga ett diagram med hjälp av en dokumentbyggare med en specificerad diagramtyp, bredd och höjd, och ta bort dess demodata.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Se även

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
