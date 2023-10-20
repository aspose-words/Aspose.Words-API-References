---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: ChartAxisTitle Text propiedad. Obtiene o establece el texto del título del eje. Sinulo o se especifica un valor vacío se mostrará el título generado automáticamente en C#.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Obtiene o establece el texto del título del eje. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente.

```csharp
public string Text { get; set; }
```

## Observaciones

Usar[`Show`](../show/) opción si necesita mostrar el título.

## Ejemplos

Muestra cómo configurar el título del eje del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Eliminar la serie generada por defecto.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Establecer título del eje.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Ver también

* class [ChartAxisTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
