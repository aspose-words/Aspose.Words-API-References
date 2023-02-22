---
title: ChartTitle.Text
second_title: Aspose.Words per .NET API Reference
description: ChartTitle proprietà. Ottiene o imposta il testo del titolo del grafico. Se viene specificato un valore nullo o vuoto verrà mostrato il titolo generato automaticamente.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Ottiene o imposta il testo del titolo del grafico. Se viene specificato un valore nullo o vuoto, verrà mostrato il titolo generato automaticamente.

```csharp
public string Text { get; set; }
```

### Osservazioni

Uso[`Show`](../show/) opzione se è necessario nascondere il titolo.

### Esempi

Mostra come inserire un grafico e impostare un titolo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma di grafico con un generatore di documenti e ottieni il suo grafico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Usa la proprietà "Titolo" per assegnare un titolo al nostro grafico, che appare in alto al centro dell'area del grafico.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Imposta la proprietà "Mostra" su "true" per rendere visibile il titolo.
title.Show = true;

// Imposta la proprietà "Overlay" su "true" Assegna più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Guarda anche

* class [ChartTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../charttitle/)
* assemblea [Aspose.Words](../../../)


