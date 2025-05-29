---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words per .NET
description: Controlla la visibilità del tuo grafico con la proprietà ChartDataTable Show. Attiva e disattiva facilmente la visualizzazione della tabella dati per ottenere informazioni più approfondite. Valore predefinito: false.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

Ottiene o imposta un flag che indica se la tabella dati verrà visualizzata per il grafico. Il valore predefinito è `falso` .

```csharp
public bool Show { get; set; }
```

## Osservazioni

I seguenti tipi di grafico non supportano tabelle dati: grafici a dispersione, a torta, ad anello, a superficie, radar, ad albero, a raggiera, a istogramma, a parete, a scatola e baffi, a cascata, a imbuto e combinati che includono serie di questi tipi. La visualizzazione di una tabella dati per questi tipi di grafico genera un errore.InvalidOperationException eccezione.

## Esempi

Mostra come visualizzare una tabella dati con dati di serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Guarda anche

* class [ChartDataTable](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
