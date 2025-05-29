---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartDataLabelCollection NumberFormat per personalizzare facilmente i formati delle etichette dati per l'intera serie, migliorandone la chiarezza e la presentazione.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Ottiene un[`ChartNumberFormat`](../../chartnumberformat/) istanza che consente di impostare il formato numerico per le etichette dati dell'intera serie .

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## Esempi

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
