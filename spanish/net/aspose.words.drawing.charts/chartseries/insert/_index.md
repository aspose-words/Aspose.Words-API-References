---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words para .NET
description: Mejore sus gráficos fácilmente con el método de inserción ChartSeries. Inserte valores X en cualquier índice y optimice la visualización de sus datos fácilmente.
type: docs
weight: 200
url: /es/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

Inserta el valor X especificado en la serie del gráfico en el índice especificado. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## Observaciones

El punto de datos correspondiente con el formato predeterminado se insertará en la colección de puntos de datos. Si se muestran etiquetas de datos, también se insertará la etiqueta de datos correspondiente con el formato predeterminado.

## Ejemplos

Muestra cómo insertar datos en una serie de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Limpia los valores X e Y de la primera serie.
series1.ClearValues();
// Rellena la serie con datos.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ver también

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

Inserta los valores X e Y especificados en la serie del gráfico en el índice especificado.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## Observaciones

El punto de datos correspondiente con el formato predeterminado se insertará en la colección de puntos de datos. Si se muestran etiquetas de datos, también se insertará la etiqueta de datos correspondiente con el formato predeterminado.

## Ejemplos

Muestra cómo insertar datos en una serie de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Limpia los valores X e Y de la primera serie.
series1.ClearValues();
// Rellena la serie con datos.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ver también

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

Inserta el valor X, el valor Y y el tamaño de burbuja especificados en la serie del gráfico en el índice especificado.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Observaciones

El punto de datos correspondiente con el formato predeterminado se insertará en la colección de puntos de datos. Si se muestran etiquetas de datos, también se insertará la etiqueta de datos correspondiente con el formato predeterminado.

## Ejemplos

Muestra cómo insertar datos en una serie de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Limpia los valores X e Y de la primera serie.
series1.ClearValues();
// Rellena la serie con datos.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ver también

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
