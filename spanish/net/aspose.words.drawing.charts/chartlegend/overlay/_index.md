---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words para .NET
description: Los elementos del gráfico de control se superponen con la propiedad ChartLegend Overlay. Mejore la visualización de datos con opciones de leyenda personalizables para obtener información más clara.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Determina si se permitirá que otros elementos del gráfico se superpongan a la leyenda. El valor predeterminado es`FALSO` .

```csharp
public bool Overlay { get; set; }
```

## Ejemplos

Muestra cómo editar la apariencia de la leyenda de un gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Mueve la leyenda del gráfico a la esquina superior derecha.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Dale más espacio a otros elementos del gráfico, como el gráfico, permitiéndoles superponerse a la leyenda.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ver también

* class [ChartLegend](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
