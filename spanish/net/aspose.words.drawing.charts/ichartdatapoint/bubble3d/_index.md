---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words para .NET
description: Descubra la propiedad IChartDataPoint Bubble3D para mejorar sus gráficos de burbujas con impresionantes efectos 3D para una visualización de datos más atractiva.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Especifica si se debe aplicar un efecto 3D a las burbujas del gráfico de burbujas.

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

//Aplica una etiqueta de datos a cada burbuja que muestre su diámetro.
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
