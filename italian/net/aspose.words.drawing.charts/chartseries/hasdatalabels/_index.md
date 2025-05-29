---
title: ChartSeries.HasDataLabels
linktitle: HasDataLabels
articleTitle: HasDataLabels
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartSeries HasDataLabels per gestire facilmente la visibilità delle etichette dati per le tue serie, migliorando la tua esperienza di visualizzazione dei dati.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chartseries/hasdatalabels/
---
## ChartSeries.HasDataLabels property

Ottiene o imposta un flag che indica se le etichette dati vengono visualizzate per la serie.

```csharp
public bool HasDataLabels { get; set; }
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

* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
