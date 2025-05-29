---
title: ChartLegend.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartLegend Format для легкой настройки заливки легенды и стилей линий, что улучшит ваши возможности визуализации данных.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartlegend/format/
---
## ChartLegend.Format property

Предоставляет доступ к заполнению и форматированию линий легенды.

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
* class [ChartLegend](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
