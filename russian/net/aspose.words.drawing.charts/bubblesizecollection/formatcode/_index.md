---
title: BubbleSizeCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BubbleSizeCollection FormatCode, чтобы легко настраивать размеры пузырьков. Улучшите визуализацию данных с помощью индивидуальных параметров форматирования.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/bubblesizecollection/formatcode/
---
## BubbleSizeCollection.FormatCode property

Возвращает или задает код формата, применяемый к размерам пузырьков.

```csharp
public string FormatCode { get; set; }
```

## Примечания

Форматирование чисел используется для изменения способа отображения значений на диаграмме. Примеры числовых форматов:

Число - "#,##0.00"

Валюта - "\"$\"#,##0.00"

Время - "[$-x-systime]ч:мм:сс AM/PM"

Дата - "д/мм/гггг"

Процент - "0.00%"

Дробь - "# ?/?"

Научное - "0.00E+00"

Бухгалтерский учет - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Пользовательский с цветом - "[Красный]-#,##0.0"

## Примеры

Показывает, как работать с кодом формата данных диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте пузырьковую диаграмму.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Показать метки данных.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Установить коды формата данных.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Смотрите также

* class [BubbleSizeCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
