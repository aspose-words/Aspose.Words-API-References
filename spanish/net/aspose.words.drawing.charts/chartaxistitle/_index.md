---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.ChartAxisTitle para administrar fácilmente las propiedades del título del eje y mejorar el impacto visual de su documento.
type: docs
weight: 910
url: /es/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Proporciona acceso a las propiedades del título del eje.

Para obtener más información, visite el[Trabajando con gráficos ](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartAxisTitle
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Proporciona acceso al formato de fuente del título del eje. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Proporciona acceso al relleno y formato de línea del título del eje. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Determina si se permitirá que otros elementos del gráfico se superpongan al título. El valor predeterminado es`FALSO` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Determina si se mostrará el título para el eje. El valor predeterminado es`FALSO` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Obtiene o establece el texto del título del eje. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente. |

## Ejemplos

Muestra cómo establecer el título del eje del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
//Eliminar serie generada por defecto.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
