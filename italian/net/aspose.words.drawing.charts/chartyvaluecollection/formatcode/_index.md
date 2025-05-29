---
title: ChartYValueCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words per .NET
description: Scopri la proprietà FormatCode di ChartYValueCollection per personalizzare facilmente la formattazione del valore Y. Migliora la visualizzazione dei tuoi dati con precisione!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartyvaluecollection/formatcode/
---
## ChartYValueCollection.FormatCode property

Ottiene o imposta il codice di formato applicato ai valori Y.

```csharp
public string FormatCode { get; set; }
```

## Osservazioni

La formattazione dei numeri viene utilizzata per modificare il modo in cui i valori vengono visualizzati nel grafico. Esempi di formati numerici:

Numero - "#,##0.00"

Valuta - "\"$\"#,##0.00"

Ora - "[$-x-systime]h:mm:ss AM/PM"

Data - "g/mm/aaaa"

Percentuale - "0,00%"

Frazione - "# ?/?"

Scientifico - "0.00E+00"

Contabilità - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Personalizzato con colore - "[Rosso]-#,##0.0"

## Esempi

Mostra come lavorare con il codice di formato dei dati del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a bolle.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Elimina la serie generata di default.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Mostra le etichette dei dati.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Imposta i codici del formato dei dati.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Guarda anche

* class [ChartYValueCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
