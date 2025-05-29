---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Diagramme mühelos mit der Add-Methode „ChartSeriesCollection“. Fügen Sie Balken-, Säulen-, Linien- und Oberflächendiagrammen nahtlos neue Serien hinzu, um dynamische Visualisierungen zu erhalten.
type: docs
weight: 30
url: /de/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

Fügt neue hinzu[`ChartSeries`](../../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu jeder Art von Balken-, Säulen-, Linien- und Oberflächendiagrammen hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Rückgabewert

Zuletzt hinzugefügt[`ChartSeries`](../../chartseries/) Objekt.

## Beispiele

Zeigt, wie ein Pareto-Diagramm erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Pareto-Diagramm ein.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

Zeigt, wie ein Trichterdiagramm erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Trichterdiagramm einfügen.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

Zeigt, wie man ein Box- und Whisker-Diagramm erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Box & Whisker-Diagramm ein.
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
ChartSeries series = chart.Series.Add(
    "Points by Years",
    new string[]
    {
        "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC",
        "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR",
        "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA"
    },
    new double[]
    {
        91, 80, 100, 77, 90, 104, 105, 118, 120, 101,
        114, 107, 110, 60, 79, 78, 77, 102, 101, 113,
        94, 93, 84, 71, 80, 103, 80, 94, 100, 101
    });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

Zeigt, wie ein geeigneter Diagrammreihentyp für einen Diagrammtyp erstellt wird.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Es gibt mehrere Möglichkeiten, die Seriensammlung eines Diagramms zu füllen.
    // Für unterschiedliche Diagrammtypen sind unterschiedliche Reihenschemata vorgesehen.
    // 1 – Säulendiagramm mit Säulen, die entlang der X-Achse nach Kategorie gruppiert und in Bänder eingeteilt sind:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Fügen Sie zwei Dezimalwertreihen ein, die für jede jeweilige Kategorie einen Wert enthalten.
    // Dieses Säulendiagramm besteht aus drei Gruppen mit jeweils zwei Säulen.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Kategorien werden entlang der X-Achse verteilt und Werte entlang der Y-Achse.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Flächendiagramm mit entlang der X-Achse verteilten Daten:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Fügt eine Reihe mit einem Dezimalwert für jedes jeweilige Datum ein.
    // Die Daten werden entlang einer linearen X-Achse verteilt,
    // und die dieser Reihe hinzugefügten Werte erstellen Datenpunkte.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-Streudiagramm:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Jede Reihe benötigt zwei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte und das zweite die entsprechenden Y-Werte
    // von Datenpunkten im Diagrammgraphen.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Blasendiagramm:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Jede Reihe benötigt drei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte, das zweite enthält die entsprechenden Y-Werte,
    // und der dritte enthält Durchmesser für jeden Datenpunkt des Diagramms.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Fügen Sie mithilfe eines Dokumentgenerators mit einem angegebenen Diagrammtyp, einer angegebenen Breite und Höhe ein Diagramm ein und entfernen Sie die Demodaten.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

Fügt neue hinzu[`ChartSeries`](../../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu jeder Art von Streudiagrammen hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Rückgabewert

Zuletzt hinzugefügt[`ChartSeries`](../../chartseries/) Objekt.

## Beispiele

Zeigt, wie ein geeigneter Diagrammreihentyp für einen Diagrammtyp erstellt wird.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Es gibt mehrere Möglichkeiten, die Seriensammlung eines Diagramms zu füllen.
    // Für unterschiedliche Diagrammtypen sind unterschiedliche Reihenschemata vorgesehen.
    // 1 – Säulendiagramm mit Säulen, die entlang der X-Achse nach Kategorie gruppiert und in Bänder eingeteilt sind:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Fügen Sie zwei Dezimalwertreihen ein, die für jede jeweilige Kategorie einen Wert enthalten.
    // Dieses Säulendiagramm besteht aus drei Gruppen mit jeweils zwei Säulen.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Kategorien werden entlang der X-Achse verteilt und Werte entlang der Y-Achse.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Flächendiagramm mit entlang der X-Achse verteilten Daten:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Fügt eine Reihe mit einem Dezimalwert für jedes jeweilige Datum ein.
    // Die Daten werden entlang einer linearen X-Achse verteilt,
    // und die dieser Reihe hinzugefügten Werte erstellen Datenpunkte.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-Streudiagramm:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Jede Reihe benötigt zwei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte und das zweite die entsprechenden Y-Werte
    // von Datenpunkten im Diagrammgraphen.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Blasendiagramm:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Jede Reihe benötigt drei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte, das zweite enthält die entsprechenden Y-Werte,
    // und der dritte enthält Durchmesser für jeden Datenpunkt des Diagramms.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Fügen Sie mithilfe eines Dokumentgenerators mit einem angegebenen Diagrammtyp, einer angegebenen Breite und Höhe ein Diagramm ein und entfernen Sie die Demodaten.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

Fügt neue hinzu[`ChartSeries`](../../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu allen Arten von Flächen-, Radar- und Aktiendiagrammen hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

## Beispiele

Zeigt, wie ein geeigneter Diagrammreihentyp für einen Diagrammtyp erstellt wird.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Es gibt mehrere Möglichkeiten, die Seriensammlung eines Diagramms zu füllen.
    // Für unterschiedliche Diagrammtypen sind unterschiedliche Reihenschemata vorgesehen.
    // 1 – Säulendiagramm mit Säulen, die entlang der X-Achse nach Kategorie gruppiert und in Bänder eingeteilt sind:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Fügen Sie zwei Dezimalwertreihen ein, die für jede jeweilige Kategorie einen Wert enthalten.
    // Dieses Säulendiagramm besteht aus drei Gruppen mit jeweils zwei Säulen.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Kategorien werden entlang der X-Achse verteilt und Werte entlang der Y-Achse.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Flächendiagramm mit entlang der X-Achse verteilten Daten:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Fügt eine Reihe mit einem Dezimalwert für jedes jeweilige Datum ein.
    // Die Daten werden entlang einer linearen X-Achse verteilt,
    // und die dieser Reihe hinzugefügten Werte erstellen Datenpunkte.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-Streudiagramm:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Jede Reihe benötigt zwei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte und das zweite die entsprechenden Y-Werte
    // von Datenpunkten im Diagrammgraphen.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Blasendiagramm:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Jede Reihe benötigt drei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte, das zweite enthält die entsprechenden Y-Werte,
    // und der dritte enthält Durchmesser für jeden Datenpunkt des Diagramms.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Fügen Sie mithilfe eines Dokumentgenerators mit einem angegebenen Diagrammtyp, einer angegebenen Breite und Höhe ein Diagramm ein und entfernen Sie die Demodaten.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

Fügt neue hinzu[`ChartSeries`](../../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu allen Arten von Blasendiagrammen hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Rückgabewert

Zuletzt hinzugefügt[`ChartSeries`](../../chartseries/) Objekt.

## Beispiele

Zeigt, wie ein geeigneter Diagrammreihentyp für einen Diagrammtyp erstellt wird.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Es gibt mehrere Möglichkeiten, die Seriensammlung eines Diagramms zu füllen.
    // Für unterschiedliche Diagrammtypen sind unterschiedliche Reihenschemata vorgesehen.
    // 1 – Säulendiagramm mit Säulen, die entlang der X-Achse nach Kategorie gruppiert und in Bänder eingeteilt sind:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Fügen Sie zwei Dezimalwertreihen ein, die für jede jeweilige Kategorie einen Wert enthalten.
    // Dieses Säulendiagramm besteht aus drei Gruppen mit jeweils zwei Säulen.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Kategorien werden entlang der X-Achse verteilt und Werte entlang der Y-Achse.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Flächendiagramm mit entlang der X-Achse verteilten Daten:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Fügt eine Reihe mit einem Dezimalwert für jedes jeweilige Datum ein.
    // Die Daten werden entlang einer linearen X-Achse verteilt,
    // und die dieser Reihe hinzugefügten Werte erstellen Datenpunkte.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-Streudiagramm:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Jede Reihe benötigt zwei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte und das zweite die entsprechenden Y-Werte
    // von Datenpunkten im Diagrammgraphen.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Blasendiagramm:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Jede Reihe benötigt drei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte, das zweite enthält die entsprechenden Y-Werte,
    // und der dritte enthält Durchmesser für jeden Datenpunkt des Diagramms.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Fügen Sie mithilfe eines Dokumentgenerators mit einem angegebenen Diagrammtyp, einer angegebenen Breite und Höhe ein Diagramm ein und entfernen Sie die Demodaten.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

Fügt neue hinzu[`ChartSeries`](../../chartseries/)zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen mit mehrstufigen Datenkategorien hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### Rückgabewert

Zuletzt hinzugefügt[`ChartSeries`](../../chartseries/) Objekt.

## Beispiele

Zeigt, wie man ein Sunburst-Diagramm erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Sunburst-Diagramm ein.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
ChartSeries series = chart.Series.Add(
    "Sales",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Sales - Europe", "UK", "London Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Liverpool Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Manchester Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Paris Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Lyon Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Denver Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Seattle Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Detroit Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Houston Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Toronto Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Montreal Dep."),
        new ChartMultilevelValue("Sales - Oceania", "Australia", "Sydney Dep."),
        new ChartMultilevelValue("Sales - Oceania", "New Zealand", "Auckland Dep.")
    },
    new double[] { 1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694 });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

Zeigt, wie ein Treemap-Diagramm erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Treemap-Diagramm ein.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

Fügt neue hinzu[`ChartSeries`](../../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu Histogrammdiagrammen hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### Rückgabewert

Zuletzt hinzugefügt[`ChartSeries`](../../chartseries/) Objekt.

## Bemerkungen

Für andere Diagrammtypen als Histogramm fügt diese Methode eine Reihe mit leeren Y-Werten hinzu.

## Beispiele

Zeigt, wie ein Histogrammdiagramm erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Histogrammdiagramm ein.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
chart.Series.Add(
    "Avg Temperature",
    new double[]
    {
        51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4,
        53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7,
        56.3, 55.9, 55.6
    });

doc.Save(ArtifactsDir + "Charts.Histogram.docx");
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

Fügt neue hinzu[`ChartSeries`](../../chartseries/) zu dieser Sammlung. Verwenden Sie diese Methode, um Reihen zu Wasserfalldiagrammen hinzuzufügen.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| seriesName | String | Ein Name der hinzuzufügenden Serie. |
| categories | String[] | Kategorienamen für die X-Achse. |
| values | Double[] | Werte der Y-Achse. |
| isSubtotal | Boolean[] | Werte, die angeben, ob der entsprechende Y-Wert eine Zwischensumme ist. |

### Rückgabewert

Zuletzt hinzugefügt[`ChartSeries`](../../chartseries/) Objekt.

## Bemerkungen

Für andere Diagrammtypen als Wasserfall,*isSubtotal* Werte werden ignoriert.

## Beispiele

Zeigt, wie man ein Wasserfalldiagramm erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Wasserfalldiagramm ein.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
