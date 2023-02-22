---
title: Enum AxisCategoryType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.AxisCategoryType перечисление. Определяет тип оси категорий.
type: docs
weight: 520
url: /ru/net/aspose.words.drawing.charts/axiscategorytype/
---
## AxisCategoryType enumeration

Определяет тип оси категорий.

```csharp
public enum AxisCategoryType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Automatic | `0` | Указывает, что тип оси категорий определяется автоматически на основе данных. |
| Category | `1` | Указывает ось произвольного набора категорий. |
| Time | `2` | Задает ось категории времени. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


