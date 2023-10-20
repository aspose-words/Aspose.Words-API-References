---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words для .NET
description: ChartLegendEntry IsHidden свойство. Получает или задает значение указывающее скрыта ли эта запись в легенде диаграммы. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Получает или задает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию:**ЛОЖЬ** .

```csharp
public bool IsHidden { get; set; }
```

## Примечания

Когда запись легенды диаграммы скрыта, это не влияет на соответствующую серию диаграммы или линию тренда, которая все еще отображается на диаграмме.

## Примеры

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

* class [ChartLegendEntry](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
