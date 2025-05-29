---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartNumberFormat для расширенного форматирования чисел в диаграммах. Улучшите визуальную привлекательность вашего документа!
type: docs
weight: 1060
url: /ru/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Представляет форматирование чисел родительского элемента.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartNumberFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Возвращает или задает код формата, применяемый к метке данных. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Указывает, связан ли код формата с исходной ячейкой. Значение по умолчанию — true. |

## Примеры

Показывает, как задать форматирование значений диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Добавить пользовательскую серию в диаграмму с категориями для оси X,
 // и большие соответствующие числовые значения для оси Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Задайте формат чисел для меток делений оси Y, чтобы не группировать цифры с запятыми.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Этот флаг может переопределить указанное выше значение и извлечь числовой формат из исходной ячейки.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
