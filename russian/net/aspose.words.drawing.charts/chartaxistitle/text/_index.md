---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartAxisTitle Text для легкой настройки названий осей. Задайте или получите динамические названия для улучшенной визуализации данных.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Возвращает или задает текст заголовка оси. Если`нулевой` или указано пустое значение, будет показан автоматически сгенерированный заголовок.

```csharp
public string Text { get; set; }
```

## Примечания

Использовать[`Show`](../show/)опция, если вам нужно показать заголовок.

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

* class [ChartAxisTitle](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
