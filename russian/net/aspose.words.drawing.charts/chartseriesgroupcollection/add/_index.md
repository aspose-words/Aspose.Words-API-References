---
title: ChartSeriesGroupCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Откройте для себя метод ChartSeriesGroupCollection Add, позволяющий легко добавлять новые группы рядов и расширять возможности визуализации данных.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---
## ChartSeriesGroupCollection.Add method

Добавляет новую группу серий указанного типа в эту коллекцию.

```csharp
public ChartSeriesGroup Add(ChartSeriesType seriesType)
```

## Примечания

Комбинированные диаграммы могут содержать группы рядов только следующих типов: площадные, линейчатые, столбчатые, линейные, круговые, точечные, лепестковые и биржевые (за исключением соответствующих типов 3D-рядов).

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

* class [ChartSeriesGroup](../../chartseriesgroup/)
* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroupCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
