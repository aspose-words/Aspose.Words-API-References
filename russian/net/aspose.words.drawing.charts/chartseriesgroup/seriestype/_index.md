---
title: ChartSeriesGroup.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeriesGroup SeriesType, чтобы легко определять типы рядов диаграмм в визуализациях данных для расширенного анализа и получения полезных сведений.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/seriestype/
---
## ChartSeriesGroup.SeriesType property

Получает тип серии диаграмм, включенных в эту группу.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Примеры

Показывает, как работать со вторичной осью диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Удалить сгенерированную по умолчанию серию.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Создаем дополнительную группу серий, также линейного типа.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Укажите использование вторичных осей для новой группы серий.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Скрыть вторичную ось X.
newSeriesGroup.AxisX.Hidden = true;
// Определить заголовок вторичной оси Y.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Добавить серию в новую группу серий.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Смотрите также

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroup](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
