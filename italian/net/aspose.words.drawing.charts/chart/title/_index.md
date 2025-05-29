---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words per .NET
description: Scopri la proprietà Titolo del grafico per una facile personalizzazione e una grafica migliorata. Sfrutta appieno il potenziale dei tuoi grafici con funzionalità intuitive!
type: docs
weight: 120
url: /it/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Fornisce accesso alle proprietà del titolo del grafico.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
