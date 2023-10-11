---
title: ChartAxisTitle.Text
second_title: Справочник по API Aspose.Words для .NET
description: ChartAxisTitle свойство. Получает или задает текст заголовка оси. Еслинулевой или указано пустое значение будет показан автоматически сгенерированный заголовок.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Получает или задает текст заголовка оси. Если`нулевой` или указано пустое значение, будет показан автоматически сгенерированный заголовок.

```csharp
public string Text { get; set; }
```

### Примечания

Использовать[`Show`](../show/) вариант, если вам нужно показать заголовок.

### Примеры

Показывает, как установить заголовок оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Удалить созданную по умолчанию серию.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Установить заголовок оси.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Смотрите также

* class [ChartAxisTitle](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* сборка [Aspose.Words](../../../)


