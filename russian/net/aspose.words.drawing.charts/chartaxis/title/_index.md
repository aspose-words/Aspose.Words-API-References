---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartAxis Title для легкого доступа и настройки названий осей, улучшая визуализацию и представление данных.
type: docs
weight: 250
url: /ru/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

Предоставляет доступ к свойствам заголовка оси.

```csharp
public ChartAxisTitle Title { get; }
```

## Примеры

Показывает, как задать заголовок оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Удалить сгенерированную по умолчанию серию.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Смотрите также

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
