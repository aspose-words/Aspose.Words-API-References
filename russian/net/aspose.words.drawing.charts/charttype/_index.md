---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.Drawing.Charts.ChartType, чтобы открыть для себя различные типы диаграмм и без труда улучшить визуализацию данных вашего документа.
type: docs
weight: 1150
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
| Area | `0` | Диаграмма областей. |
| AreaStacked | `1` | Диаграмма с накоплением областей. |
| AreaPercentStacked | `2` | 100%-ная диаграмма с накоплением областей. |
| Area3D | `3` | 3D Диаграмма областей. |
| Area3DStacked | `4` | 3D-диаграмма с накоплением областей. |
| Area3DPercentStacked | `5` | 3D 100% составная диаграмма областей. |
| Bar | `6` | Гистограмма. |
| BarStacked | `7` | Сложенная столбчатая диаграмма. |
| BarPercentStacked | `8` | 100%-ная столбчатая диаграмма с накоплением. |
| Bar3D | `9` | 3D-линейная диаграмма. |
| Bar3DStacked | `10` | 3D-график с накоплением. |
| Bar3DPercentStacked | `11` | 3D 100% штабелированная столбчатая диаграмма. |
| Bubble | `12` | Пузырьковая диаграмма. |
| Bubble3D | `13` | 3D пузырьковая диаграмма. |
| Column | `14` | Столбчатая диаграмма. |
| ColumnStacked | `15` | Столбчатая диаграмма с накоплением. |
| ColumnPercentStacked | `16` | 100%-ная столбчатая диаграмма с накоплением. |
| Column3D | `17` | 3D Столбчатая диаграмма. |
| Column3DStacked | `18` | 3D-столбчатая диаграмма с накоплением. |
| Column3DPercentStacked | `19` | 3D 100% столбчатая диаграмма с накоплением. |
| Column3DClustered | `20` | 3D кластеризованная столбчатая диаграмма. |
| Doughnut | `21` | Кольцевая диаграмма. |
| Line | `22` | Линейный график. |
| LineStacked | `23` | Сложенная линейная диаграмма. |
| LinePercentStacked | `24` | 100%-ная линейная диаграмма с накоплением. |
| Line3D | `25` | 3D Линейный график. |
| Pie | `26` | Круговая диаграмма. |
| Pie3D | `27` | 3D круговая диаграмма. |
| PieOfBar | `28` | Круговая диаграмма. |
| PieOfPie | `29` | Круговая диаграмма. |
| Radar | `30` | Радарная диаграмма. |
| Scatter | `31` | Диаграмма рассеяния. |
| Stock | `32` | График акций. |
| Surface | `33` | Поверхностная диаграмма. |
| Surface3D | `34` | 3D Поверхностная диаграмма. |
| Treemap | `35` | Диаграмма древовидной карты. |
| Sunburst | `36` | Диаграмма солнечных лучей. |
| Histogram | `37` | Гистограмма. |
| Pareto | `38` | Диаграмма Парето. |
| BoxAndWhisker | `39` | Диаграмма «ящик с усами». |
| Waterfall | `40` | Водопадная диаграмма. |
| Funnel | `41` | Воронкообразная диаграмма. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
