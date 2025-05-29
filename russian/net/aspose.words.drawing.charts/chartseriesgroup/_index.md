---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartSeriesGroup, который упрощает управление свойствами рядов диаграмм для улучшенной визуализации и анализа данных.
type: docs
weight: 1090
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Представляет свойства группы рядов диаграмм, то есть свойства рядов диаграмм одного типа , связанных с одними и теми же осями.

```csharp
public class ChartSeriesGroup
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Возвращает или задает группу осей, к которой принадлежит данная группа серий. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Предоставляет доступ к свойствам оси X этой группы серий. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Предоставляет доступ к свойствам оси Y этой группы серий. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Возвращает или задает размер пузырьков в процентах от их размера по умолчанию. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Возвращает или задает размер отверстия родительской кольцевой диаграммы в процентах. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Возвращает или задает угол в градусах первого сектора родительской круговой диаграммы. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Возвращает или задает процент ширины зазора между элементами диаграммы. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Возвращает или задает процент перекрытия столбцов или полос ряда. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Возвращает или задает размер вторичной секции круговой диаграммы в процентах. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Получает коллекцию серий, принадлежащих этой группе серий. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Получает тип серии диаграмм, включенных в эту группу. |

## Примечания

Комбинированные диаграммы содержат несколько групп серий диаграмм, при этом для каждого типа серии существует отдельная группа.

Кроме того, вы можете создать группу серий диаграмм, чтобы назначить вторичные оси одной или нескольким сериям диаграмм.

Чтобы узнать больше, посетите[ Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
