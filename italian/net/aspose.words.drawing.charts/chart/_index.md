---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words per .NET
description: Sblocca potenti proprietà delle forme dei grafici con la classe Aspose.Words.Drawing.Charts.Chart. Arricchisci i tuoi documenti con una rappresentazione visiva dinamica dei dati.
type: docs
weight: 880
url: /it/net/aspose.words.drawing.charts/chart/
---
## Chart class

Fornisce accesso alle proprietà della forma del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class Chart
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Ottiene una raccolta di tutti gli assi di questo grafico. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Fornisce l'accesso alle proprietà dell'asse X primario del grafico. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Fornisce l'accesso alle proprietà dell'asse Y primario del grafico. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Fornisce l'accesso alle proprietà dell'asse Z del grafico. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Fornisce l'accesso alle proprietà di una tabella dati di questo grafico. La tabella dati può essere visualizzata utilizzando[`Show`](../chartdatatable/show/) proprietà. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Fornisce accesso al riempimento e alla formattazione delle linee del grafico. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Fornisce accesso alle proprietà della legenda del grafico. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Fornisce accesso alla raccolta di serie. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Fornisce l'accesso a una raccolta di gruppi di serie di questo grafico. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Ottiene il percorso e il nome di un file xls/xlsx a cui è collegato questo grafico. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Ottiene o imposta lo stile del grafico. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Fornisce accesso alle proprietà del titolo del grafico. |

## Esempi

Mostra come inserire un grafico e impostare un titolo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma di grafico con un generatore di documenti e ottieni il relativo grafico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilizziamo la proprietà "Titolo" per assegnare un titolo al nostro grafico, che verrà visualizzato al centro, in alto, dell'area del grafico.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // Imposta la proprietà "Show" su "true" per rendere visibile il titolo.
title.Show = true;

// Imposta la proprietà "Sovrapposizione" su "vero" Dai più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
