---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxis NumberFormat per personalizzare senza sforzo i formati numerici del tuo grafico con l'oggetto ChartNumberFormat per una visualizzazione avanzata dei dati.
type: docs
weight: 200
url: /it/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Restituisce un[`ChartNumberFormat`](../../chartnumberformat/) oggetto che consente di definire formati numerici per l'asse.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## Esempi

Mostra come impostare la formattazione per i valori del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiungi una serie personalizzata al grafico con categorie per l'asse X,
 // e rispettivi valori numerici grandi per l'asse Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Imposta il formato numerico delle etichette delle tacche dell'asse Y in modo da non raggruppare le cifre con virgole.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Questo flag può sovrascrivere il valore soprastante e ricavare il formato numerico dalla cella di origine.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Guarda anche

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
