---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.Charts.ChartSeriesType per migliorare le tue serie di grafici con diverse opzioni per la visualizzazione dinamica dei dati.
type: docs
weight: 1110
url: /it/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Specifica un tipo di serie di grafici.

```csharp
public enum ChartSeriesType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Area | `0` | Rappresenta una serie di grafici ad area. |
| AreaStacked | `1` | Rappresenta una serie di grafici ad area impilata. |
| AreaPercentStacked | `2` | Rappresenta una serie di grafici ad area impilata al 100%. |
| Area3D | `3` | Rappresenta una serie di grafici ad area 3D. |
| Area3DStacked | `4` | Rappresenta una serie di grafici ad area impilata 3D. |
| Area3DPercentStacked | `5` | Rappresenta una serie di grafici 3D ad area impilata al 100%. |
| Bar | `6` | Rappresenta una serie di grafici a barre. |
| BarStacked | `7` | Rappresenta una serie di grafici a barre impilate. |
| BarPercentStacked | `8` | Rappresenta una serie di grafici a barre impilate al 100%. |
| Bar3D | `9` | Rappresenta una serie di grafici a barre 3D. |
| Bar3DStacked | `10` | Rappresenta una serie di grafici a barre impilate 3D. |
| Bar3DPercentStacked | `11` | Rappresenta una serie di grafici a barre impilate 3D al 100%. |
| Bubble | `12` | Rappresenta una serie di grafici a bolle. |
| Bubble3D | `13` | Rappresenta una serie di grafici a bolle 3D. |
| Column | `14` | Rappresenta una serie di grafici a colonne. |
| ColumnStacked | `15` | Rappresenta una serie di grafici a colonne impilate. |
| ColumnPercentStacked | `16` | Rappresenta una serie di grafici a colonne impilate al 100%. |
| Column3D | `17` | Rappresenta una serie di grafici a colonne 3D. |
| Column3DStacked | `18` | Rappresenta una serie di grafici a colonne impilate 3D. |
| Column3DPercentStacked | `19` | Rappresenta una serie di grafici a colonne impilate 3D al 100%. |
| Column3DClustered | `20` | Rappresenta una serie di grafici a colonne raggruppate 3D. |
| Doughnut | `21` | Rappresenta una serie di grafici a ciambella. |
| Line | `22` | Rappresenta una serie di grafici a linee. |
| LineStacked | `23` | Rappresenta una serie di grafici a linee impilate. |
| LinePercentStacked | `24` | Rappresenta una serie di grafici a linee impilate al 100%. |
| Line3D | `25` | Rappresenta una serie di grafici a linee 3D. |
| Pie | `26` | Rappresenta una serie di grafici a torta. |
| Pie3D | `27` | Rappresenta una serie di grafici a torta 3D. |
| PieOfBar | `28` | Rappresenta una serie di grafici a torta o a barre. |
| PieOfPie | `29` | Rappresenta una serie di grafici a torta. |
| Radar | `30` | Rappresenta una serie di grafici radar. |
| Scatter | `31` | Rappresenta una serie di grafici a dispersione. |
| Stock | `32` | Rappresenta una serie di grafici azionari. |
| Surface | `33` | Rappresenta una serie di grafici di superficie. |
| Surface3D | `34` | Rappresenta una serie di grafici di superficie 3D. |
| Treemap | `35` | Rappresenta una serie di grafici Treemap. |
| Sunburst | `36` | Rappresenta una serie di grafici Sunburst. |
| Histogram | `37` | Rappresenta una serie di grafici a istogramma. |
| Pareto | `38` | Rappresenta una serie di grafici di Pareto. |
| ParetoLine | `39` | Rappresenta una serie di grafici a linee di Pareto. |
| BoxAndWhisker | `40` | Rappresenta una serie di grafici a scatola e baffi. |
| Waterfall | `41` | Rappresenta una serie di grafici a cascata. |
| Funnel | `42` | Rappresenta una serie di grafici a imbuto. |
| RegionMap | `43` | Rappresenta una serie di grafici della mappa regionale. |

## Esempi

Mostra come rimuovere serie specifiche di grafici.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Rimuove tutte le serie di tipo Colonna.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
