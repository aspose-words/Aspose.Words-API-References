---
title: ChartSeriesCollection.Add
second_title: Справочник по API Aspose.Words для .NET
description: ChartSeriesCollection метод. Добавляет новыеChartSeries в эту коллекцию. Используйте этот метод для добавления рядов в линейчатые столбчатые линейные и поверхностные диаграммы любого типа.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(string, string[], double[]) {#add_3}

Добавляет новые[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления рядов в линейчатые, столбчатые, линейные и поверхностные диаграммы любого типа.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Возвращаемое значение

Недавно добавленный[`ChartSeries`](../../chartseries/) объект.

### Примеры

Показывает, как создать серию диаграмм, соответствующую типу диаграммы.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции серий диаграммы.
    // Разные схемы серий предназначены для разных типов диаграмм.
    // 1 — столбчатая диаграмма со столбцами, сгруппированными и распределенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставляем две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет состоять из трех групп, каждая из которых состоит из двух столбцов.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Категории распределяются по оси X, а значения — по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями с датами, распределенными по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставляем серию с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные в эту серию, создадут точки данных.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-диаграмма рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуется два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй — соответствующие значения Y
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
    // Первый массив содержит значения X, второй содержит соответствующие значения Y,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с помощью построителя документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
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
* пространство имен [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* сборка [Aspose.Words](../../../)

---

## Add(string, double[], double[]) {#add}

Добавляет новые[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий в точечные диаграммы любого типа.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Возвращаемое значение

Недавно добавленный[`ChartSeries`](../../chartseries/) объект.

### Примеры

Показывает, как создать серию диаграмм, соответствующую типу диаграммы.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции серий диаграммы.
    // Разные схемы серий предназначены для разных типов диаграмм.
    // 1 — столбчатая диаграмма со столбцами, сгруппированными и распределенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставляем две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет состоять из трех групп, каждая из которых состоит из двух столбцов.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Категории распределяются по оси X, а значения — по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями с датами, распределенными по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставляем серию с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные в эту серию, создадут точки данных.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-диаграмма рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуется два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй — соответствующие значения Y
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
    // Первый массив содержит значения X, второй содержит соответствующие значения Y,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с помощью построителя документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
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
* пространство имен [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* сборка [Aspose.Words](../../../)

---

## Add(string, DateTime[], double[]) {#add_2}

Добавляет новые[`ChartSeries`](../../chartseries/) в эту коллекцию. Используйте этот метод для добавления серий к любым типам площадных, радарных и биржевых диаграмм.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

### Примеры

Показывает, как создать серию диаграмм, соответствующую типу диаграммы.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции серий диаграммы.
    // Разные схемы серий предназначены для разных типов диаграмм.
    // 1 — столбчатая диаграмма со столбцами, сгруппированными и распределенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставляем две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет состоять из трех групп, каждая из которых состоит из двух столбцов.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Категории распределяются по оси X, а значения — по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями с датами, распределенными по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставляем серию с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные в эту серию, создадут точки данных.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-диаграмма рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуется два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй — соответствующие значения Y
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
    // Первый массив содержит значения X, второй содержит соответствующие значения Y,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с помощью построителя документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
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
* пространство имен [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* сборка [Aspose.Words](../../../)

---

## Add(string, double[], double[], double[]) {#add_1}

Добавляет новые[`ChartSeries`](../../chartseries/)в эту коллекцию. Используйте этот метод для добавления рядов в пузырьковые диаграммы любого типа.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Возвращаемое значение

Недавно добавленный[`ChartSeries`](../../chartseries/) объект.

### Примеры

Показывает, как создать серию диаграмм, соответствующую типу диаграммы.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции серий диаграммы.
    // Разные схемы серий предназначены для разных типов диаграмм.
    // 1 — столбчатая диаграмма со столбцами, сгруппированными и распределенными вдоль оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставляем две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет состоять из трех групп, каждая из которых состоит из двух столбцов.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Категории распределяются по оси X, а значения — по оси Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Диаграмма с областями с датами, распределенными по оси X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Вставляем серию с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные в эту серию, создадут точки данных.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-диаграмма рассеяния:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуется два десятичных массива одинаковой длины.
    // Первый массив содержит значения X, а второй — соответствующие значения Y
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
    // Первый массив содержит значения X, второй содержит соответствующие значения Y,
    // а третий содержит диаметры для каждой точки данных графика.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с помощью построителя документов указанного типа диаграммы, ширины и высоты и удалите ее демонстрационные данные.
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
* пространство имен [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* сборка [Aspose.Words](../../../)


