---
title: AxisTickLabels.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words для .NET
description: Управляйте интервалами AxisTickLabels без усилий! Установите интервалы для меток делений, чтобы улучшить визуализацию данных и повысить ясность диаграммы.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing.charts/axisticklabels/spacing/
---
## AxisTickLabels.Spacing property

Возвращает или задает интервал, с которым отрисовываются метки делений.

```csharp
public int Spacing { get; set; }
```

## Примечания

Свойство действует на текстовые категории и оси серий. Оно не поддерживается MS Office 2016 new charts. Допустимый диапазон значений больше или равен 1.

Установка этого свойства устанавливает[`IsAutoSpacing`](../isautospacing/) собственность`ЛОЖЬ`.

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

* class [AxisTickLabels](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
