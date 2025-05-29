---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartLegend para mejorar sus gráficos con propiedades de leyenda personalizables para una mejor visualización de datos.
type: docs
weight: 1010
url: /es/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Representa las propiedades de la leyenda del gráfico.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartLegend
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Proporciona acceso al formato de fuente predeterminado de las entradas de leyenda. Para anular el formato de fuente de una entrada de leyenda específica, utilice el comando[`Font`](../chartlegendentry/font/) propiedad. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Proporciona acceso al relleno y formato de línea de la leyenda. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Devuelve una colección de entradas de leyenda para todas las series y líneas de tendencia del gráfico principal. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Determina si se permitirá que otros elementos del gráfico se superpongan a la leyenda. El valor predeterminado es`FALSO` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Especifica la posición de la leyenda en un gráfico. |

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
