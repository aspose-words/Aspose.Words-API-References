---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ChartNumberFormat IsLinkedToSource улучшает визуализацию данных, связывая коды формата с исходными ячейками. Узнайте больше прямо сейчас!
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Указывает, связан ли код формата с исходной ячейкой. Значение по умолчанию — true.

```csharp
public bool IsLinkedToSource { get; set; }
```

## Примечания

Формат NumberFormat будет сброшен до общего, если код формата связан с источником.

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

* class [ChartNumberFormat](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
