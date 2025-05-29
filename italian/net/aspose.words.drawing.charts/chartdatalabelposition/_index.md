---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ChartDataLabelPosition per personalizzare facilmente le etichette dei dati del grafico, per una maggiore chiarezza e presentazione.
type: docs
weight: 960
url: /it/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Specifica la posizione per un'etichetta dati del grafico.

```csharp
public enum ChartDataLabelPosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Center | `0` | Specifica che un'etichetta dati deve essere visualizzata centrata su un indicatore di dati. |
| Left | `1` | Specifica che un'etichetta dati deve essere visualizzata a sinistra di un indicatore di dati. |
| Right | `2` | Specifica che un'etichetta dati deve essere visualizzata a destra di un indicatore di dati. |
| Above | `3` | Specifica che un'etichetta dati deve essere visualizzata sopra un indicatore di dati. |
| Below | `4` | Specifica che un'etichetta dati deve essere visualizzata sotto un indicatore di dati. |
| InsideBase | `5` | Specifica che un'etichetta dati deve essere visualizzata all'interno della base di un marcatore dati. |
| InsideEnd | `6` | Specifica che un'etichetta dati deve essere visualizzata all'interno della fine di un marcatore dati. |
| OutsideEnd | `7` | Specifica che un'etichetta dati deve essere visualizzata all'esterno della fine di un marcatore dati. |
| BestFit | `8` | Specifica che un'etichetta dati deve essere visualizzata nella posizione più appropriata. |

## Osservazioni

Non tutti i tipi di serie consentono di specificare le posizioni delle etichette. E quelli che lo consentono, non supportano tutti i valori.

## Esempi

Mostra come impostare la posizione dell'etichetta dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a colonne.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Elimina la serie generata di default.
seriesColl.Clear();

// Aggiungi serie.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Mostra le etichette dei dati e imposta il colore del carattere.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Imposta la posizione dell'etichetta dati.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
