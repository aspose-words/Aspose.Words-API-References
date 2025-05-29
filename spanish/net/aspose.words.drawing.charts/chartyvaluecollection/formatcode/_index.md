---
title: ChartYValueCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartYValueCollection FormatCode para personalizar fácilmente el formato del valor Y. ¡Mejore la visualización de sus datos con precisión!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartyvaluecollection/formatcode/
---
## ChartYValueCollection.FormatCode property

Obtiene o establece el código de formato aplicado a los valores Y.

```csharp
public string FormatCode { get; set; }
```

## Observaciones

El formato de números se utiliza para cambiar la forma en que aparecen los valores en el gráfico. Ejemplos de formatos de números:

Número - "#,##0.00"

Moneda - "\"$\"#,##0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/aaaa"

Porcentaje - "0,00%"

Fracción - "# ?/?

Científico - "0.00E+00"

Contabilidad - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Personalizado con color - "[Rojo]-#,##0.0"

## Ejemplos

Muestra cómo trabajar con el código de formato de los datos del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de burbujas.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

//Eliminar serie generada por defecto.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Establecer códigos de formato de datos.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Ver también

* class [ChartYValueCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
