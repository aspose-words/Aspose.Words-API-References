---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ChartFormat для расширенного стиля элементов диаграммы. Улучшите свои документы с помощью профессиональных, настраиваемых дизайнов диаграмм.
type: docs
weight: 1000
url: /ru/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Представляет форматирование элемента диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Получает форматирование заливки для родительского элемента диаграммы. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Получает флаг, указывающий, определен ли какой-либо формат. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Возвращает или задает тип фигуры родительского элемента диаграммы. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Получает форматирование строки для родительского элемента диаграммы. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Сбрасывает заливку элемента диаграммы на значение по умолчанию. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
