---
title: AxisGroup Enum
linktitle: AxisGroup
articleTitle: AxisGroup
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.Charts.AxisGroup, la chiave per gestire in modo efficace i gruppi di assi dei grafici per una migliore visualizzazione dei dati.
type: docs
weight: 800
url: /it/net/aspose.words.drawing.charts/axisgroup/
---
## AxisGroup enumeration

Rappresenta un tipo di gruppo di assi del grafico.

```csharp
public enum AxisGroup
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Primary | `0` | Specifica il gruppo di assi primario. |
| Secondary | `1` | Specifica il gruppo di assi secondari. |

## Esempi

Mostra come lavorare con l'asse secondario del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Elimina la serie generata di default.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Crea un gruppo di serie aggiuntivo, anch'esso di tipo linea.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Specificare l'uso di assi secondari per il nuovo gruppo di serie.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Nascondi l'asse X secondario.
newSeriesGroup.AxisX.Hidden = true;
// Definisce il titolo dell'asse Y secondario.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Aggiunge una serie al nuovo gruppo di serie.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
