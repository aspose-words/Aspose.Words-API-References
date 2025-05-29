---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words для .NET
description: Легко улучшайте свои диаграммы с помощью метода ChartSeries Insert. Вставляйте значения X в любой индекс, с легкостью оптимизируя визуализацию данных!
type: docs
weight: 200
url: /ru/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

Вставляет указанное значение X в ряд диаграммы по указанному индексу. Если ряд поддерживает значения Y и размеры пузырьков, они будут пустыми для значения X.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## Примечания

Соответствующая точка данных с форматированием по умолчанию будет вставлена в коллекцию точек данных. И, если отображаются метки данных, соответствующая метка данных с форматированием по умолчанию также будет вставлена.

## Примеры

Показывает, как вставлять данные в ряд диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();
// Заполняем ряд данными.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

Вставляет указанные значения X и Y в ряд диаграммы по указанному индексу.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## Примечания

Соответствующая точка данных с форматированием по умолчанию будет вставлена в коллекцию точек данных. И, если отображаются метки данных, соответствующая метка данных с форматированием по умолчанию также будет вставлена.

## Примеры

Показывает, как вставлять данные в ряд диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();
// Заполняем ряд данными.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

Вставляет указанное значение X, значение Y и размер пузырька в ряд диаграммы по указанному индексу.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Примечания

Соответствующая точка данных с форматированием по умолчанию будет вставлена в коллекцию точек данных. И, если отображаются метки данных, соответствующая метка данных с форматированием по умолчанию также будет вставлена.

## Примеры

Показывает, как вставлять данные в ряд диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();
// Заполняем ряд данными.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
