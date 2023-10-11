---
title: Enum ChartType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartType перечисление. Указывает тип диаграммы.
type: docs
weight: 830
url: /ru/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Указывает тип диаграммы.

```csharp
public enum ChartType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Area | `0` | Диаграмма площади. |
| AreaStacked | `1` | Диаграмма с областями с накоплением. |
| AreaPercentStacked | `2` | Диаграмма с 100% суммированием площадей. |
| Area3D | `3` | Трехмерная диаграмма области. |
| Area3DStacked | `4` | 3D-диаграмма с областями с накоплением. |
| Area3DPercentStacked | `5` | 3D-диаграмма со 100% суммированной площадью. |
| Bar | `6` | Гистограмма. |
| BarStacked | `7` | Гистограмма с накоплением. |
| BarPercentStacked | `8` | Столбчатая диаграмма со 100% накоплением. |
| Bar3D | `9` | 3D-линейчатая диаграмма. |
| Bar3DStacked | `10` | 3D-диаграмма с накоплением. |
| Bar3DPercentStacked | `11` | 3D гистограмма со 100% накоплением. |
| Bubble | `12` | Пузырьковая диаграмма. |
| Bubble3D | `13` | Пузырьковая 3D-диаграмма. |
| Column | `14` | Столбчатая диаграмма. |
| ColumnStacked | `15` | Столбчатая диаграмма с накоплением. |
| ColumnPercentStacked | `16` | Столбчатая диаграмма со 100% накоплением. |
| Column3D | `17` | 3D-столбчатая диаграмма. |
| Column3DStacked | `18` | 3D-столбчатая диаграмма с накоплением. |
| Column3DPercentStacked | `19` | 3D-столбчатая диаграмма со 100% накоплением. |
| Column3DClustered | `20` | 3D кластеризованная столбчатая диаграмма. |
| Doughnut | `21` | Кольцевая диаграмма. |
| Line | `22` | Линейный график. |
| LineStacked | `23` | Линейная диаграмма с накоплением. |
| LinePercentStacked | `24` | Линейная диаграмма со 100% накоплением. |
| Line3D | `25` | 3D-линейная диаграмма. |
| Pie | `26` | Круговая диаграмма. |
| Pie3D | `27` | Круговая 3D-диаграмма. |
| PieOfBar | `28` | Круговая диаграмма. |
| PieOfPie | `29` | Круговая диаграмма. |
| Radar | `30` | Радарная диаграмма. |
| Scatter | `31` | Точечная диаграмма. |
| Stock | `32` | Биржевой график. |
| Surface | `33` | Поверхностная диаграмма. |
| Surface3D | `34` | Трехмерная диаграмма поверхности. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


