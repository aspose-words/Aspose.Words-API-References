---
title: AxisCrosses Enum
linktitle: AxisCrosses
articleTitle: AxisCrosses
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.AxisCrosses перечисление. Указывает возможные точки пересечения оси на С#.
type: docs
weight: 540
url: /ru/net/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enumeration

Указывает возможные точки пересечения оси.

```csharp
public enum AxisCrosses
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Automatic | `0` | Ось категорий пересекается в нулевой точке оси значений (если возможно) или в минимальном значении , если минимум больше нуля, или в максимуме, если максимум меньше нуля. |
| Maximum | `1` | Перпендикулярная ось пересекает максимальное значение оси. |
| Minimum | `2` | Перпендикулярная ось пересекает минимальное значение оси. |
| Custom | `3` | Перпендикулярная ось пересекает указанное значение оси. |

## Примеры

Показывает, как вставить диаграмму и изменить внешний вид ее осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставляем серию диаграмм с категориями для оси X и соответствующими числовыми значениями для оси Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Оси диаграммы имеют различные параметры, которые могут изменить их внешний вид,
// такие как их направление, такты основных/второстепенных единиц и деления.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Столбчатые диаграммы не имеют оси Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
