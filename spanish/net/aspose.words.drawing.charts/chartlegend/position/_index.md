---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: Descubra la propiedad Posición de leyenda de gráfico para personalizar fácilmente la ubicación de la leyenda de su gráfico para lograr una mayor claridad y atractivo visual.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Especifica la posición de la leyenda en un gráfico.

```csharp
public LegendPosition Position { get; set; }
```

## Observaciones

El valor predeterminado esRight para gráficos anteriores a Word 2016 y Top para gráficos de Word 2016.

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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
