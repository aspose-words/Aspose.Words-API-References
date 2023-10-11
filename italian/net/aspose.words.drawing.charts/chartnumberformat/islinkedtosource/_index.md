---
title: ChartNumberFormat.IsLinkedToSource
second_title: Aspose.Words per .NET API Reference
description: ChartNumberFormat proprietà. Specifica se il codice del formato è collegato a una cella di origine. Il valore predefinito è true.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Specifica se il codice del formato è collegato a una cella di origine. Il valore predefinito è true.

```csharp
public bool IsLinkedToSource { get; set; }
```

### Osservazioni

NumberFormat verrà reimpostato su generale se il codice del formato è collegato all'origine.

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

* class [ChartNumberFormat](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartnumberformat/)
* assemblea [Aspose.Words](../../../)


