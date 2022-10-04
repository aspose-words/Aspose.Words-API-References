---
title: ChartType
second_title: Справочник по API Aspose.Words для .NET
description: Задает тип диаграммы.
type: docs
weight: 760
url: /ru/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Задает тип диаграммы.

```csharp
public enum ChartType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Area | `0` | Диаграмма с областями. |
| AreaStacked | `1` | Диаграмма с областями с накоплением. |
| AreaPercentStacked | `2` | 100%-ная диаграмма областей с накоплением. |
| Area3D | `3` | Трехмерная диаграмма с областями. |
| Area3DStacked | `4` | Трехмерная диаграмма с накоплением областей. |
| Area3DPercentStacked | `5` | 3D-диаграмма со 100 % суммированием областей. |
| Bar | `6` | Гистограмма. |
| BarStacked | `7` | Гистограмма с накоплением. |
| BarPercentStacked | `8` | 100% гистограмма с накоплением. |
| Bar3D | `9` | Трехмерная гистограмма. |
| Bar3DStacked | `10` | Трехмерная линейчатая диаграмма с накоплением. |
| Bar3DPercentStacked | `11` | 3D 100% гистограмма с накоплением. |
| Bubble | `12` | Пузырьковая диаграмма. |
| Bubble3D | `13` | 3D пузырьковая диаграмма. |
| Column | `14` | Столбчатая диаграмма. |
| ColumnStacked | `15` | Столбчатая диаграмма с накоплением. |
| ColumnPercentStacked | `16` | 100% столбчатая диаграмма с накоплением. |
| Column3D | `17` | 3D Столбчатая диаграмма. |
| Column3DStacked | `18` | Трехмерная столбчатая диаграмма с накоплением. |
| Column3DPercentStacked | `19` | 3D 100% столбчатая диаграмма с накоплением. |
| Column3DClustered | `20` | 3D-гистограмма с кластерами. |
| Doughnut | `21` | Кольцевая диаграмма. |
| Line | `22` | Линейный график. |
| LineStacked | `23` | График с накоплением. |
| LinePercentStacked | `24` | 100% линейная диаграмма с суммированием. |
| Line3D | `25` | Трехмерная линейная диаграмма. |
| Pie | `26` | Круговая диаграмма. |
| Pie3D | `27` | Трехмерная круговая диаграмма. |
| PieOfBar | `28` | Круговая гистограмма. |
| PieOfPie | `29` | Круговая диаграмма. |
| Radar | `30` | Радиолокационная карта. |
| Scatter | `31` | Точечная диаграмма. |
| Stock | `32` | Биржевой график. |
| Surface | `33` | Поверхностная диаграмма. |
| Surface3D | `34` | 3D-диаграмма поверхности. |

### Примеры

Показывает, как создать подходящий тип серии диаграмм для типа графика.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Существует несколько способов заполнения коллекции серий диаграммы.
    // Разные схемы серий предназначены для разных типов графиков.
    // 1 - Столбчатая диаграмма со столбцами, сгруппированными и распределенными по оси X по категориям:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Вставьте две серии десятичных значений, содержащих значение для каждой соответствующей категории.
    // Эта столбчатая диаграмма будет состоять из трех групп, в каждой из которых будет по два столбца.
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

    // Вставить ряд с десятичным значением для каждой соответствующей даты.
    // Даты будут распределены по линейной оси X,
    // и значения, добавленные к этому ряду, создадут точки данных.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D точечная диаграмма:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Для каждой серии потребуется два десятичных массива одинаковой длины.
    // Первый массив содержит X-значения, а второй содержит соответствующие Y-значения
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
    // а третий содержит диаметры для каждой из точек данных графика.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Вставьте диаграмму с помощью построителя документов указанного типа ChartType, ширины и высоты и удалите ее демонстрационные данные.
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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
