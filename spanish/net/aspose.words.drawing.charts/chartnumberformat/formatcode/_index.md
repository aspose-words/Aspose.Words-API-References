---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad FormatCode de ChartNumberFormat para personalizar los formatos de etiquetas de datos para obtener información más clara y una mejor presentación de los datos.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Obtiene o establece el código de formato aplicado a una etiqueta de datos.

```csharp
public string FormatCode { get; set; }
```

## Observaciones

El formato de números se utiliza para cambiar la forma en que aparece un valor en la etiqueta de datos y se puede utilizar de maneras muy creativas. Los ejemplos de formatos de números:

Número - "#,##0.00"

Moneda - "\"$\"#,##0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/aaaa"

Porcentaje - "0,00%"

Fracción - "# ?/?

Científico - "0.00E+00"

Texto - "@"

Contabilidad - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Personalizado con color - "[Rojo]-#,##0.0"

## Ejemplos

Muestra cómo establecer el formato para los valores del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada al gráfico con categorías para el eje X,
 // y valores numéricos grandes respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Establezca el formato de número de las etiquetas de marca del eje Y para no agrupar los dígitos con comas.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Esta bandera puede anular el valor anterior y extraer el formato de número de la celda de origen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

Muestra cómo habilitar y configurar etiquetas de datos para una serie de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue un gráfico de líneas, luego borre su serie de datos de demostración para comenzar con un gráfico limpio.
// y luego establece un título.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Insertar una serie de gráficos personalizados con meses como categorías para el eje X,
// y los respectivos decimales para el eje Y.
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

* class [ChartNumberFormat](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
