---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.Charts.ChartTitle classe. Fornisce laccesso alle proprietà del titolo del grafico in C#.
type: docs
weight: 820
url: /it/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Fornisce l'accesso alle proprietà del titolo del grafico.

Per saperne di più, visita il[Lavorare con grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartTitle
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Determina se altri elementi del grafico possono sovrapporsi al titolo. Per impostazione predefinita la sovrapposizione è`falso` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Determina se il titolo deve essere mostrato per questo grafico. Il valore predefinito è`VERO` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Ottiene o imposta il testo del titolo del grafico. Se`nullo` o viene specificato un valore vuoto, verrà mostrato il titolo generato automaticamente. |

## Esempi

Mostra come inserire un grafico e impostare un titolo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma di grafico con un generatore di documenti e ottieni il suo grafico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilizza la proprietà "Titolo" per assegnare un titolo al nostro grafico, che appare in alto al centro dell'area del grafico.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Imposta la proprietà "Mostra" su "true" per rendere visibile il titolo.
title.Show = true;

// Imposta la proprietà "Overlay" su "true" Concede più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
