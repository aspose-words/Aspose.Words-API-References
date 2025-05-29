---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeries LegendEntry para acceder y personalizar fácilmente las entradas de leyenda de sus gráficos, mejorando la visualización de sus datos.
type: docs
weight: 90
url: /es/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Obtiene una entrada de leyenda para esta serie de gráficos.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Ejemplos

Muestra cómo trabajar con una fuente de leyenda.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Establecer el tamaño de fuente predeterminado para todas las entradas de leyenda.
chartLegend.Font.Size = 14;
// Cambiar la fuente para una entrada de leyenda específica.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Obtener la entrada de leyenda para la serie de gráficos.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Ver también

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
