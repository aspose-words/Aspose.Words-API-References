---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: ChartLegend Position propiedad. Especifica la posición de la leyenda en un gráfico. El valor predeterminado esRight  en C#.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Especifica la posición de la leyenda en un gráfico. El valor predeterminado esRight .

```csharp
public LegendPosition Position { get; set; }
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

// Da más espacio a otros elementos del gráfico, como el gráfico, permitiéndoles superponerse a la leyenda.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ver también

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
