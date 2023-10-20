---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: ChartDataLabelCollection Font propiedad. Proporciona acceso al formato de fuente de las etiquetas de datos de toda la serie en C#.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Proporciona acceso al formato de fuente de las etiquetas de datos de toda la serie.

```csharp
public Font Font { get; }
```

## Observaciones

El valor definido para esta propiedad se puede anular para una etiqueta de datos individual usando the [`Font`](../../chartdatalabel/font/) propiedad.

## Ejemplos

Muestra cómo habilitar y configurar etiquetas de datos para una serie de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue un gráfico de líneas, luego borre su serie de datos de demostración para comenzar con un gráfico limpio,
// y luego establece un título.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Inserta una serie de gráficos personalizados con meses como categorías para el eje X,
// y respectivas cantidades decimales para el eje Y.
ChartSeries series = chart.Series.Add("Revenue", 
    new[] { "January", "February", "March" }, 
    new[] { 25.611d, 21.439d, 33.750d });

// Habilite las etiquetas de datos y luego aplique un formato de número personalizado para los valores que se muestran en las etiquetas de datos.
// Este formato tratará los valores decimales mostrados como millones de dólares estadounidenses.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;            

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Ver también

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
