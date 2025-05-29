---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words для .NET
description: Откройте для себя метод ChartXValue FromString для легкого создания экземпляров ChartXValue типа String. Улучшите визуализацию данных сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Создает[`ChartXValue`](../) примерString тип.

```csharp
public static ChartXValue FromString(string value)
```

## Примеры

Показывает, как добавлять/удалять значения данных диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Удалить первое значение в обеих сериях.
department1Series.Remove(0);
department2Series.Remove(0);

// Добавляем новые значения в обе серии.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Смотрите также

* class [ChartXValue](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
