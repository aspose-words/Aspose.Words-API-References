---
title: ChartAxis.MinorTickMark
linktitle: MinorTickMark
articleTitle: MinorTickMark
second_title: Aspose.Words для .NET
description: Настройте ChartAxis с помощью свойства MinorTickMark, чтобы повысить точность осей и улучшить визуализацию данных. Легко устанавливайте или возвращайте второстепенные деления!
type: docs
weight: 160
url: /ru/net/aspose.words.drawing.charts/chartaxis/minortickmark/
---
## ChartAxis.MinorTickMark property

Возвращает или задает вспомогательные деления для оси.

```csharp
public AxisTickMark MinorTickMark { get; set; }
```

## Примеры

Показывает, как вставить диаграмму и изменить внешний вид ее осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставьте ряд диаграмм с категориями для оси X и соответствующими числовыми значениями для оси Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Оси диаграммы имеют различные параметры, которые могут изменить их внешний вид,
// например, их направление, основные/дополнительные деления и отметки делений.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Столбчатые диаграммы не имеют оси Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Смотрите также

* enum [AxisTickMark](../../axistickmark/)
* class [ChartAxis](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
