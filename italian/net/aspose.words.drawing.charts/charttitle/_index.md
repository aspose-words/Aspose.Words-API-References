---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartTitle per gestire e personalizzare facilmente i titoli dei grafici per una migliore visualizzazione dei dati.
type: docs
weight: 1140
url: /it/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Fornisce accesso alle proprietà del titolo del grafico.

Per saperne di più, visita il[Lavorare con i grafici ](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartTitle
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Fornisce accesso alla formattazione del carattere del titolo del grafico. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Fornisce accesso al riempimento e alla formattazione delle linee del titolo del grafico. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Determina se altri elementi del grafico possono sovrapporsi al titolo. Per impostazione predefinita, la sovrapposizione è`falso` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Determina se il titolo deve essere visualizzato per questo grafico. Il valore predefinito è`VERO` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Ottiene o imposta il testo del titolo del grafico. Se`null` o se viene specificato un valore vuoto, verrà mostrato il titolo generato automaticamente. |

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
