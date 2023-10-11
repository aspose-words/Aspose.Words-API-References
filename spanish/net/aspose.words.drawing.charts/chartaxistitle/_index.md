---
title: Class ChartAxisTitle
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle clase. Proporciona acceso a las propiedades del título del eje.
type: docs
weight: 650
url: /es/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Proporciona acceso a las propiedades del título del eje.

Para obtener más información, visite el[Trabajar con gráficos ](https://docs.aspose.com/words/net/working-with-charts/) artículo de documentación.

```csharp
public class ChartAxisTitle
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Determina si se permitirá que otros elementos del gráfico se superpongan al título. El valor predeterminado es`FALSO` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Determina si se mostrará el título para el eje. El valor predeterminado es`FALSO` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Obtiene o establece el texto del título del eje. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente. |

### Ejemplos

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)


