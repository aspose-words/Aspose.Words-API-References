---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Легко улучшайте свои диаграммы с помощью метода ChartSeriesCollection Add. Легко добавляйте новые серии в столбчатые, линейные, поверхностные диаграммы для динамических визуальных эффектов.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

Добавляет новый[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в любые типы линейчатых, столбчатых, линейных и поверхностных диаграмм.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Возвращаемое значение

Недавно добавлено[`ChartSeries`](../../chartseries/) объект.

## Примеры

Показывает, как создать диаграмму Парето.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте диаграмму Парето.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

Показывает, как создать воронкообразную диаграмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте воронкообразную диаграмму.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// Показать метки данных.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

Показывает, как создать диаграмму «ящик с усами».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте диаграмму «ящик с усами».
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
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

// Показать метки данных.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

Показывает, как создать подходящий тип серии диаграмм для определенного типа графика.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции рядов диаграммы.
    // Различные схемы рядов предназначены для различных типов диаграмм.
    // 1 — Столбчатая диаграмма со столбцами, сгруппированными и разделенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставьте две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет иметь три группы, каждая из которых будет состоять из двух столбцов.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Категории распределены по оси X, а значения распределены по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями, где даты распределены по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставьте ряд с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные к этому ряду, создадут точки данных.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-график рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуются два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй содержит соответствующие значения Y
    // точек данных на графике диаграммы.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Пузырьковая диаграмма:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Для каждой серии потребуется три десятичных массива одинаковой длины.
    // Первый массив содержит X-значения, второй содержит соответствующие Y-значения,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с использованием конструктора документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

Добавляет новый[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в любые типы диаграмм рассеяния.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Возвращаемое значение

Недавно добавлено[`ChartSeries`](../../chartseries/) объект.

## Примеры

Показывает, как создать подходящий тип серии диаграмм для определенного типа графика.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции рядов диаграммы.
    // Различные схемы рядов предназначены для различных типов диаграмм.
    // 1 — Столбчатая диаграмма со столбцами, сгруппированными и разделенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставьте две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет иметь три группы, каждая из которых будет состоять из двух столбцов.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Категории распределены по оси X, а значения распределены по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями, где даты распределены по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставьте ряд с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные к этому ряду, создадут точки данных.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-график рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуются два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй содержит соответствующие значения Y
    // точек данных на графике диаграммы.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Пузырьковая диаграмма:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Для каждой серии потребуется три десятичных массива одинаковой длины.
    // Первый массив содержит X-значения, второй содержит соответствующие Y-значения,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с использованием конструктора документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

Добавляет новый[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в любые типы площадных, радиальных и биржевых диаграмм.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

## Примеры

Показывает, как создать подходящий тип серии диаграмм для определенного типа графика.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции рядов диаграммы.
    // Различные схемы рядов предназначены для различных типов диаграмм.
    // 1 — Столбчатая диаграмма со столбцами, сгруппированными и разделенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставьте две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет иметь три группы, каждая из которых будет состоять из двух столбцов.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Категории распределены по оси X, а значения распределены по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями, где даты распределены по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставьте ряд с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные к этому ряду, создадут точки данных.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-график рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуются два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй содержит соответствующие значения Y
    // точек данных на графике диаграммы.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Пузырьковая диаграмма:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Для каждой серии потребуется три десятичных массива одинаковой длины.
    // Первый массив содержит X-значения, второй содержит соответствующие Y-значения,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с использованием конструктора документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

Добавляет новый[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в любые типы пузырьковых диаграмм.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Возвращаемое значение

Недавно добавлено[`ChartSeries`](../../chartseries/) объект.

## Примеры

Показывает, как создать подходящий тип серии диаграмм для определенного типа графика.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции рядов диаграммы.
    // Различные схемы рядов предназначены для различных типов диаграмм.
    // 1 — Столбчатая диаграмма со столбцами, сгруппированными и разделенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставьте две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет иметь три группы, каждая из которых будет состоять из двух столбцов.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Категории распределены по оси X, а значения распределены по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями, где даты распределены по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставьте ряд с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные к этому ряду, создадут точки данных.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-график рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуются два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй содержит соответствующие значения Y
    // точек данных на графике диаграммы.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Пузырьковая диаграмма:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Для каждой серии потребуется три десятичных массива одинаковой длины.
    // Первый массив содержит X-значения, второй содержит соответствующие Y-значения,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с использованием конструктора документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

Добавляет новый[`ChartSeries`](../../chartseries/)в эту коллекцию. Используйте этот метод для добавления рядов, имеющих многоуровневые категории данных.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### Возвращаемое значение

Недавно добавлено[`ChartSeries`](../../chartseries/) объект.

## Примеры

Показывает, как создать диаграмму солнечных лучей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте диаграмму Sunburst.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
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

// Показать метки данных.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

Показывает, как создать древовидную диаграмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить диаграмму Treemap.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
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

// Показать метки данных.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

Добавляет новый[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в гистограммы.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### Возвращаемое значение

Недавно добавлено[`ChartSeries`](../../chartseries/) объект.

## Примечания

Для типов диаграмм, отличных от гистограммы, этот метод добавляет ряд с пустыми значениями Y.

## Примеры

Показывает, как создать гистограмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте гистограмму.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
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

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

Добавляет новый[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в каскадные диаграммы.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| seriesName | String | Название серии, которая будет добавлена. |
| categories | String[] | Названия категорий для оси X. |
| values | Double[] | Значения по оси Y. |
| isSubtotal | Boolean[] | Значения, указывающие, является ли соответствующее значение Y промежуточным итогом. |

### Возвращаемое значение

Недавно добавлено[`ChartSeries`](../../chartseries/) объект.

## Примечания

Для типов диаграмм, отличных от каскадных,*isSubtotal* значения игнорируются.

## Примеры

Показывает, как создать каскадную диаграмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте каскадную диаграмму.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Показать метки данных.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### Смотрите также

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
