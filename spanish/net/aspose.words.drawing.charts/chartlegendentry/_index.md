---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.ChartLegendEntry para crear leyendas de gráficos dinámicas. Mejore la visualización de sus datos con una integración y personalización perfectas.
type: docs
weight: 1020
url: /es/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Representa una entrada de leyenda de gráfico.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartLegendEntry
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Proporciona acceso al formato de fuente de esta entrada de leyenda. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Obtiene o establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es**FALSO** . |

## Observaciones

Una entrada de leyenda corresponde a una serie de gráficos o una línea de tendencia específicas.

El texto de la entrada es el nombre de la serie o línea de tendencia. No se puede modificar.

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
