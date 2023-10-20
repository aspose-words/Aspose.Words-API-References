---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: ChartSeries Add método. Agrega el valor X especificado a la serie del gráfico. Si la serie admite valores Y y tamaños de burbujas estarán vacíos para el valor X en C#.
type: docs
weight: 160
url: /es/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Agrega el valor X especificado a la serie del gráfico. Si la serie admite valores Y y tamaños de burbujas, estarán vacíos para el valor X.

```csharp
public void Add(ChartXValue xValue)
```

### Ver también

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Agrega los valores X e Y especificados a la serie del gráfico.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
```

## Ejemplos

Muestra cómo agregar/eliminar valores de datos del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Elimina el primer valor de ambas series.
department1Series.Remove(0);
department2Series.Remove(0);

// Agrega nuevos valores a ambas series.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

Muestra cómo completar series de gráficos con datos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Borrar los valores X e Y de la primera serie.
series1.ClearValues();

// Completa la serie con datos.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// Borrar los valores X e Y de la segunda serie.
series2.ClearValues();

// Completa la serie con datos.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ver también

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Agrega el valor X, el valor Y y el tamaño de burbuja especificados a la serie del gráfico.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

### Ver también

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
