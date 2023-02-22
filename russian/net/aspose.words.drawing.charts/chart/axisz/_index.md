---
title: Chart.AxisZ
second_title: Справочник по API Aspose.Words для .NET
description: Chart свойство. Предоставляет доступ к свойствам оси Z диаграммы.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chart/axisz/
---
## Chart.AxisZ property

Предоставляет доступ к свойствам оси Z диаграммы.

```csharp
public ChartAxis AxisZ { get; }
```

### Примеры

Показывает, как вставить диаграмму и изменить внешний вид ее осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Очистить серию демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставьте серию диаграммы с категориями для оси X и соответствующими числовыми значениями для оси Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Оси диаграммы имеют различные параметры, которые могут изменить их внешний вид,
// такие как их направление, основные/второстепенные деления единиц и деления.
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

* class [ChartAxis](../../chartaxis/)
* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chart/)
* сборка [Aspose.Words](../../../)


