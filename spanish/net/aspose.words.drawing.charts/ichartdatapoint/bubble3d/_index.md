---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words para .NET
description: IChartDataPoint Bubble3D propiedad. Especifica si las burbujas en el gráfico de burbujas deben tener aplicado un efecto 3D en C#.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Especifica si las burbujas en el gráfico de burbujas deben tener aplicado un efecto 3D.

```csharp
public bool Bubble3D { get; set; }
```

## Ejemplos

Muestra cómo utilizar efectos 3D con gráficos de burbujas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Aplicar una etiqueta de datos a cada burbuja que muestre su diámetro.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Ver también

* interface [IChartDataPoint](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
