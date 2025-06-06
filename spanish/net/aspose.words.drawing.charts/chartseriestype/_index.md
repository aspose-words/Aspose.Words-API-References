---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.Charts.ChartSeriesType para mejorar su serie de gráficos con diversas opciones para la visualización dinámica de datos.
type: docs
weight: 1110
url: /es/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Especifica un tipo de serie de gráficos.

```csharp
public enum ChartSeriesType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Area | `0` | Representa una serie de gráficos de área. |
| AreaStacked | `1` | Representa una serie de gráficos de áreas apiladas. |
| AreaPercentStacked | `2` | Representa una serie de gráficos de área apilada al 100%. |
| Area3D | `3` | Representa una serie de gráficos de área 3D. |
| Area3DStacked | `4` | Representa una serie de gráficos de áreas apiladas en 3D. |
| Area3DPercentStacked | `5` | Representa una serie de gráficos de área apilada al 100 % en 3D. |
| Bar | `6` | Representa una serie de gráficos de barras. |
| BarStacked | `7` | Representa una serie de gráficos de barras apiladas. |
| BarPercentStacked | `8` | Representa una serie de gráficos de barras apiladas al 100%. |
| Bar3D | `9` | Representa una serie de gráficos de barras 3D. |
| Bar3DStacked | `10` | Representa una serie de gráficos de barras apiladas en 3D. |
| Bar3DPercentStacked | `11` | Representa una serie de gráficos de barras apiladas al 100 % en 3D. |
| Bubble | `12` | Representa una serie de gráficos de burbujas. |
| Bubble3D | `13` | Representa una serie de gráficos de burbujas 3D. |
| Column | `14` | Representa una serie de gráficos de columnas. |
| ColumnStacked | `15` | Representa una serie de gráficos de columnas apiladas. |
| ColumnPercentStacked | `16` | Representa una serie de gráficos de columnas apiladas al 100%. |
| Column3D | `17` | Representa una serie de gráficos de columnas 3D. |
| Column3DStacked | `18` | Representa una serie de gráficos de columnas apiladas en 3D. |
| Column3DPercentStacked | `19` | Representa una serie de gráficos de columnas apiladas al 100 % en 3D. |
| Column3DClustered | `20` | Representa una serie de gráficos de columnas agrupadas en 3D. |
| Doughnut | `21` | Representa una serie de gráficos de anillos. |
| Line | `22` | Representa una serie de gráficos de líneas. |
| LineStacked | `23` | Representa una serie de gráficos de líneas apiladas. |
| LinePercentStacked | `24` | Representa una serie de gráficos de líneas apiladas al 100%. |
| Line3D | `25` | Representa una serie de gráficos de líneas 3D. |
| Pie | `26` | Representa una serie de gráficos circulares. |
| Pie3D | `27` | Representa una serie de gráficos circulares 3D. |
| PieOfBar | `28` | Representa una serie de gráficos circulares o de barras. |
| PieOfPie | `29` | Representa una serie de gráficos circulares. |
| Radar | `30` | Representa una serie de gráficos de radar. |
| Scatter | `31` | Representa una serie de gráficos de dispersión. |
| Stock | `32` | Representa una serie de gráficos de acciones. |
| Surface | `33` | Representa una serie de gráficos de superficie. |
| Surface3D | `34` | Representa una serie de gráficos de superficie 3D. |
| Treemap | `35` | Representa una serie de gráficos de mapa de árbol. |
| Sunburst | `36` | Representa una serie de gráficos Sunburst. |
| Histogram | `37` | Representa una serie de gráficos de histograma. |
| Pareto | `38` | Representa una serie de gráficos de Pareto. |
| ParetoLine | `39` | Representa una serie de gráficos de líneas de Pareto. |
| BoxAndWhisker | `40` | Representa una serie de gráficos de caja y bigotes. |
| Waterfall | `41` | Representa una serie de gráficos en cascada. |
| Funnel | `42` | Representa una serie de gráficos de embudo. |
| RegionMap | `43` | Representa una serie de gráficos de mapas de regiones. |

## Ejemplos

Muestra cómo eliminar una serie de gráficos específica.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

//Eliminar todas las series del tipo Columna.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
