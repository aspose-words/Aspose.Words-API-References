---
title: ChartAxis.NumberFormat
second_title: Aspose.Words per .NET API Reference
description: ChartAxis proprietà. Restituisce aChartNumberFormat oggetto che consente di definire i formati numerici per lasse.
type: docs
weight: 190
url: /it/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Restituisce a[`ChartNumberFormat`](../../chartnumberformat/) oggetto che consente di definire i formati numerici per l'asse.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Esempi

Mostra come impostare la formattazione per i valori del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Cancella le serie di dati dimostrativi del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiungi una serie personalizzata al grafico con categorie per l'asse X,
 // e rispettivi valori numerici grandi per l'asse Y.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Imposta il formato numerico delle etichette dei segni di spunta dell'asse Y per non raggruppare le cifre con virgole.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Questo flag può sovrascrivere il valore precedente e ricavare il formato numerico dalla cella di origine.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Guarda anche

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartaxis/)
* assemblea [Aspose.Words](../../../)


