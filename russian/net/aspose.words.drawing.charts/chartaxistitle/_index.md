---
title: Class ChartAxisTitle
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle сорт. Предоставляет доступ к свойствам заголовка оси.
type: docs
weight: 650
url: /ru/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Предоставляет доступ к свойствам заголовка оси.

Чтобы узнать больше, посетите[Работа с диаграммами ](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartAxisTitle
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. Значение по умолчанию:`ЛОЖЬ` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Определяет, будет ли отображаться заголовок для оси. Значение по умолчанию:`ЛОЖЬ` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Получает или задает текст заголовка оси. Если`нулевой` или указано пустое значение, будет показан автоматически сгенерированный заголовок. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


