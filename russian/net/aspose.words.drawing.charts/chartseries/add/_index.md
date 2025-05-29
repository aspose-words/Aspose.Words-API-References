---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: Откройте для себя метод ChartSeries Add, который позволяет легко интегрировать значения X в ваши диаграммы. Улучшите визуализацию данных с поддержкой значений Y и размеров пузырьков.
type: docs
weight: 160
url: /ru/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Добавляет указанное значение X к серии диаграмм. Если серия поддерживает значения Y и размеры пузырьков, они будут пустыми для значения X.

```csharp
public void Add(ChartXValue xValue)
```

## Примеры

Показывает, как заполнить ряды диаграмм данными.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();

// Заполняем ряд данными.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Очистить значения X и Y второй серии.
series2.Clear();

// Заполняем ряд данными.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Добавляет указанные значения X и Y в ряд диаграммы.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
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

Показывает, как заполнить ряды диаграмм данными.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();

// Заполняем ряд данными.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Очистить значения X и Y второй серии.
series2.Clear();

// Заполняем ряд данными.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Добавляет указанное значение X, значение Y и размер пузырька к серии диаграммы.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Примеры

Показывает, как заполнить ряды диаграмм данными.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();

// Заполняем ряд данными.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Очистить значения X и Y второй серии.
series2.Clear();

// Заполняем ряд данными.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
