---
title: Chart.Title
second_title: Aspose.Words per .NET API Reference
description: Chart proprietà. Fornisce laccesso alle proprietà del titolo del grafico.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Fornisce l'accesso alle proprietà del titolo del grafico.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chart/)
* assemblea [Aspose.Words](../../../)


