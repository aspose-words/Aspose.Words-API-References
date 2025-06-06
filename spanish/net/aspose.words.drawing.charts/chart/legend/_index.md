---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words para .NET
description: Descubra la propiedad Leyenda de Gráficos para personalizar sus gráficos fácilmente. Mejore la visualización de datos con opciones de leyenda personalizadas para obtener una mejor perspectiva.
type: docs
weight: 70
url: /es/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Proporciona acceso a las propiedades de la leyenda del gráfico.

```csharp
public ChartLegend Legend { get; }
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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
