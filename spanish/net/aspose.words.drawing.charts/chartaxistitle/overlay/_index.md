---
title: ChartAxisTitle.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxisTitle Overlay, que controla la superposición de elementos del gráfico para una visualización más clara. ¡Mejore la presentación de sus datos sin esfuerzo!
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartaxistitle/overlay/
---
## ChartAxisTitle.Overlay property

Determina si se permitirá que otros elementos del gráfico se superpongan al título. El valor predeterminado es`FALSO` .

```csharp
public bool Overlay { get; set; }
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

* class [ChartAxisTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
