---
title: Class ChartLegend
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartLegend clase. Representa las propiedades de la leyenda del gráfico.
type: docs
weight: 680
url: /es/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Representa las propiedades de la leyenda del gráfico.

```csharp
public class ChartLegend
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Devuelve una colección de entradas de leyenda para todas las series y líneas de tendencia del gráfico principal. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Determina si se permitirá que otros elementos del gráfico se superpongan a la leyenda. El valor predeterminado es falso. |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Especifica la posición de la leyenda en un gráfico. El valor predeterminado esRight . |

### Ejemplos

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)


