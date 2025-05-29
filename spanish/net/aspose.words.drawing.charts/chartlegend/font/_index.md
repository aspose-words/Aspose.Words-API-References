---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: ¡Personaliza la configuración de fuentes de ChartLegend fácilmente! Accede al formato predeterminado y modifica fácilmente entradas específicas de la leyenda para una apariencia impecable.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Proporciona acceso al formato de fuente predeterminado de las entradas de leyenda. Para anular el formato de fuente de una entrada de leyenda específica, utilice el comando[`Font`](../../chartlegendentry/font/) propiedad.

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
* class [ChartLegend](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
