---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: ChartDataLabel Font propiedad. Proporciona acceso al formato de fuente de esta etiqueta de datos en C#.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Proporciona acceso al formato de fuente de esta etiqueta de datos.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
