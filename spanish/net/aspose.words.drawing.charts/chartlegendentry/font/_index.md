---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: Descubra la propiedad de fuente ChartLegendEntry para acceder fácilmente al formato de fuente personalizable y mejorar sus entradas de leyenda para un mejor atractivo visual.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Proporciona acceso al formato de fuente de esta entrada de leyenda.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
