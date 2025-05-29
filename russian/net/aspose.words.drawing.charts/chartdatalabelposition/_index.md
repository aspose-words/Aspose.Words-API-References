---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.ChartDataLabelPosition, чтобы легко настраивать метки данных диаграммы для повышения ясности и наглядности.
type: docs
weight: 960
url: /ru/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Указывает положение метки данных диаграммы.

```csharp
public enum ChartDataLabelPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Center | `0` | Указывает, что метка данных должна отображаться по центру маркера данных. |
| Left | `1` | Указывает, что метка данных должна отображаться слева от маркера данных. |
| Right | `2` | Указывает, что метка данных должна отображаться справа от маркера данных. |
| Above | `3` | Указывает, что метка данных должна отображаться над маркером данных. |
| Below | `4` | Указывает, что метка данных должна отображаться под маркером данных. |
| InsideBase | `5` | Указывает, что метка данных должна отображаться внутри основания маркера данных. |
| InsideEnd | `6` | Указывает, что метка данных должна отображаться внутри конца маркера данных. |
| OutsideEnd | `7` | Указывает, что метка данных должна отображаться за пределами конца маркера данных. |
| BestFit | `8` | Указывает, что метка данных должна отображаться в наиболее подходящем месте. |

## Примечания

Не все типы серий позволяют указывать позиции меток. А те, которые позволяют, не поддерживают все значения.

## Примеры

Показывает, как задать положение метки данных.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить столбчатую диаграмму.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Удалить сгенерированную по умолчанию серию.
seriesColl.Clear();

// Добавить серию.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Отображение меток данных и установка цвета шрифта.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Установить позицию метки данных.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
