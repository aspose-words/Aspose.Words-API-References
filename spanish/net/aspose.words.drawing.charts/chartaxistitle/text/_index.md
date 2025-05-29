---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxisTitle Text para personalizar fácilmente los títulos de sus ejes. Configure u obtenga títulos dinámicos para una mejor visualización de datos.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Obtiene o establece el texto del título del eje. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente.

```csharp
public string Text { get; set; }
```

## Observaciones

Usar[`Show`](../show/)Opción si necesita mostrar el título.

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

* class [ChartAxisTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
