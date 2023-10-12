---
title: Class ChartLegendEntryCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartLegendEntryCollection сорт. Представляет коллекцию записей легенды диаграммы.
type: docs
weight: 740
url: /ru/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

Представляет коллекцию записей легенды диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | Возвращает количество[`ChartLegendEntry`](../chartlegendentry/) в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | Возвращает[`ChartLegendEntry`](../chartlegendentry/) для указанного индекса. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | Возвращает объект перечислителя. |

### Примеры

Показывает, как работать с записью легенды для серий диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Смотрите также

* class [ChartLegendEntry](../chartlegendentry/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


