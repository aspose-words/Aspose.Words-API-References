---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà FormatCode di ChartNumberFormat per personalizzare i formati delle etichette dati, ottenendo così informazioni più chiare e una presentazione dei dati migliore.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Ottiene o imposta il codice di formato applicato a un'etichetta dati.

```csharp
public string FormatCode { get; set; }
```

## Osservazioni

La formattazione dei numeri viene utilizzata per modificare il modo in cui un valore appare nell'etichetta dati e può essere utilizzata in modi molto creativi. Esempi di formati numerici:

Numero - "#,##0.00"

Valuta - "\"$\"#,##0.00"

Ora - "[$-x-systime]h:mm:ss AM/PM"

Data - "g/mm/aaaa"

Percentuale - "0,00%"

Frazione - "# ?/?"

Scientifico - "0.00E+00"

Testo - "@"

Contabilità - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Personalizzato con colore - "[Rosso]-#,##0.0"

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

Mostra come abilitare e configurare le etichette dati per una serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungi un grafico a linee, quindi cancella la serie di dati demo per iniziare con un grafico pulito,
// e quindi imposta un titolo.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Inserisci una serie di grafici personalizzati con i mesi come categorie per l'asse X,
// e rispettivi importi decimali per l'asse Y.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// Abilita le etichette dati, quindi applica un formato numerico personalizzato per i valori visualizzati nelle etichette dati.
// Questo formato tratterà i valori decimali visualizzati come milioni di dollari USA.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Guarda anche

* class [ChartNumberFormat](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
