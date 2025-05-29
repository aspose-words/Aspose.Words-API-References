---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.ChartAxisTitle, чтобы легко управлять свойствами заголовка осей и улучшить визуальное воздействие вашего документа.
type: docs
weight: 910
url: /ru/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Предоставляет доступ к свойствам заголовка оси.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartAxisTitle
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Предоставляет доступ к форматированию шрифта заголовка оси. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Предоставляет доступ к заполнению и форматированию строк заголовка оси. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать заголовок. Значение по умолчанию:`ЛОЖЬ` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Определяет, будет ли отображаться заголовок оси. Значение по умолчанию:`ЛОЖЬ` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Возвращает или задает текст заголовка оси. Если`нулевой` или указано пустое значение, будет показан автоматически сгенерированный заголовок. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
