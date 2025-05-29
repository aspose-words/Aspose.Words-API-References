---
title: Chart.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words для .NET
description: Откройте для себя расширенное форматирование диаграмм с помощью нашего инструмента! Легко настраивайте стили заливки и линий для создания потрясающих профессиональных визуальных эффектов, которые улучшат представление ваших данных.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing.charts/chart/format/
---
## Chart.Format property

Предоставляет доступ к заполнению и форматированию линий диаграммы.

```csharp
public ChartFormat Format { get; }
```

## Примеры

Показывает, как использовать форматирование диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Удалить серию, созданную по умолчанию.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Форматировать фон диаграммы.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Скрыть метки делений осей.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Форматировать заголовок диаграммы.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Форматировать заголовок оси.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Формат легенды.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Смотрите также

* class [ChartFormat](../../chartformat/)
* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
