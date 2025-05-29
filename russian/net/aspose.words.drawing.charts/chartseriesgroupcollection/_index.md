---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.ChartSeriesGroupCollection — ваше идеальное решение для легкого управления и организации объектов ChartSeriesGroup.
type: docs
weight: 1100
url: /ru/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Представляет собой коллекцию[`ChartSeriesGroup`](../chartseriesgroup/) объекты.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Возвращает количество групп серий в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Возвращает[`ChartSeriesGroup`](../chartseriesgroup/) по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Добавляет новую группу серий указанного типа в эту коллекцию. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Возвращает объект перечислителя. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Удаляет группу серий по указанному индексу. Все дочерние серии будут удалены из диаграммы. |

## Примечания

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
