---
title: ChartAxisTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: Personalice su ChartAxisTitle con opciones de fuente versátiles. Mejore la visualización de datos con un formato único de título de eje para una visión más clara.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartaxistitle/font/
---
## ChartAxisTitle.Font property

Proporciona acceso al formato de fuente del título del eje.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ChartAxisTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
