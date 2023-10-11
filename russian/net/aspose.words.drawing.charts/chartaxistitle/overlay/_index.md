---
title: ChartAxisTitle.Overlay
second_title: Справочник по API Aspose.Words для .NET
description: ChartAxisTitle свойство. Определяет разрешено ли другим элементам диаграммы перекрывать заголовок. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartaxistitle/overlay/
---
## ChartAxisTitle.Overlay property

Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool Overlay { get; set; }
```

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


