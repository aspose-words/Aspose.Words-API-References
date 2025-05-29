---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ChartNumberFormat IsLinkedToSource migliora la visualizzazione dei dati collegando i codici di formato alle celle di origine. Scopri di più ora!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Specifica se il codice formato è collegato a una cella di origine. Il valore predefinito è true.

```csharp
public bool IsLinkedToSource { get; set; }
```

## Osservazioni

NumberFormat verrà reimpostato su generale se il codice del formato è collegato alla sorgente.

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

* class [ChartNumberFormat](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
