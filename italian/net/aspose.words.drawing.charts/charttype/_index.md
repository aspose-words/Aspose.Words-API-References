---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.Drawing.Charts.ChartType per scoprire vari tipi di grafici e migliorare senza sforzo la visualizzazione dei dati del tuo documento.
type: docs
weight: 1150
url: /it/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Specifica il tipo di un grafico.

```csharp
public enum ChartType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Area | `0` | Grafico ad area. |
| AreaStacked | `1` | Grafico ad area impilata. |
| AreaPercentStacked | `2` | Grafico ad area impilata al 100%. |
| Area3D | `3` | Grafico ad area 3D. |
| Area3DStacked | `4` | Grafico ad area impilata 3D. |
| Area3DPercentStacked | `5` | Grafico ad area impilata 3D al 100%. |
| Bar | `6` | Grafico a barre. |
| BarStacked | `7` | Grafico a barre impilate. |
| BarPercentStacked | `8` | Grafico a barre impilate al 100%. |
| Bar3D | `9` | Grafico a barre 3D. |
| Bar3DStacked | `10` | Grafico a barre impilate 3D. |
| Bar3DPercentStacked | `11` | Grafico a barre impilate 3D al 100%. |
| Bubble | `12` | Grafico a bolle. |
| Bubble3D | `13` | Grafico a bolle 3D. |
| Column | `14` | Grafico a colonne. |
| ColumnStacked | `15` | Grafico a colonne impilate. |
| ColumnPercentStacked | `16` | Grafico a colonne impilate al 100%. |
| Column3D | `17` | Grafico a colonne 3D. |
| Column3DStacked | `18` | Grafico a colonne impilate 3D. |
| Column3DPercentStacked | `19` | Grafico a colonne impilate 3D al 100%. |
| Column3DClustered | `20` | Grafico a colonne raggruppate 3D. |
| Doughnut | `21` | Grafico a ciambella. |
| Line | `22` | Grafico a linee. |
| LineStacked | `23` | Grafico a linee impilate. |
| LinePercentStacked | `24` | Grafico a linee impilate al 100%. |
| Line3D | `25` | Grafico a linee 3D. |
| Pie | `26` | Grafico a torta. |
| Pie3D | `27` | Grafico a torta 3D. |
| PieOfBar | `28` | Grafico a torta o a barre. |
| PieOfPie | `29` | Grafico a torta. |
| Radar | `30` | Grafico radar. |
| Scatter | `31` | Grafico a dispersione. |
| Stock | `32` | Grafico azionario. |
| Surface | `33` | Carta di superficie. |
| Surface3D | `34` | Grafico di superficie 3D. |
| Treemap | `35` | Grafico ad albero. |
| Sunburst | `36` | Grafico a raggiera. |
| Histogram | `37` | Grafico istogramma. |
| Pareto | `38` | Grafico di Pareto. |
| BoxAndWhisker | `39` | Grafico a scatola e baffi. |
| Waterfall | `40` | Grafico a cascata. |
| Funnel | `41` | Grafico a imbuto. |

## Esempi

Mostra come creare un tipo appropriato di serie di grafici per un tipo di grafico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Esistono diversi modi per popolare la raccolta di serie di un grafico.
    // Diversi schemi di serie sono pensati per diversi tipi di grafici.
    // 1 - Grafico a colonne con colonne raggruppate e disposte lungo l'asse X per categoria:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserire due serie di valori decimali contenenti un valore per ciascuna rispettiva categoria.
    // Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Grafico ad area con date distribuite lungo l'asse X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserire una serie con un valore decimale per ogni rispettiva data.
    // Le date saranno distribuite lungo un asse X lineare,
    // e i valori aggiunti a questa serie creeranno punti dati.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagramma di dispersione 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Ogni serie necessiterà di due array decimali di uguale lunghezza.
    // Il primo array contiene i valori X e il secondo contiene i corrispondenti valori Y
    // dei punti dati sul grafico del grafico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Grafico a bolle:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Ogni serie necessiterà di tre array decimali di uguale lunghezza.
    // Il primo array contiene i valori X, il secondo contiene i corrispondenti valori Y,
    // e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserire un grafico utilizzando un generatore di documenti con un ChartType, larghezza e altezza specificati e rimuovere i relativi dati demo.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
