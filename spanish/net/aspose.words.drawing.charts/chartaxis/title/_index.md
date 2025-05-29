---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxis Title para acceder fácilmente y personalizar los títulos de los ejes, mejorando la visualización y presentación de sus datos.
type: docs
weight: 250
url: /es/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

Proporciona acceso a las propiedades del título del eje.

```csharp
public ChartAxisTitle Title { get; }
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

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
