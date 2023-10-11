---
title: ChartSeries.Remove
second_title: Справочник по API Aspose.Words для .NET
description: ChartSeries метод. Удаляет значение X значение Y и размер пузырька если поддерживается из серии диаграмм по указанному индексу. Соответствующая точка данных и метка данных также удаляются.
type: docs
weight: 210
url: /ru/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Удаляет значение X, значение Y и размер пузырька, если поддерживается, из серии диаграмм по указанному индексу. Соответствующая точка данных и метка данных также удаляются.

```csharp
public void Remove(int index)
```

### Примеры

Показывает, как добавлять/удалять значения данных диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Удаляем первое значение в обеих сериях.
department1Series.Remove(0);
department2Series.Remove(0);

// Добавляем новые значения в обе серии.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Смотрите также

* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chartseries/)
* сборка [Aspose.Words](../../../)


