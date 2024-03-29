---
title: ChartTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words per .NET
description: ChartTitle Show proprietà. Determina se il titolo deve essere mostrato per questo grafico. Il valore predefinito èVERO  in C#.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Determina se il titolo deve essere mostrato per questo grafico. Il valore predefinito è`VERO` .

```csharp
public bool Show { get; set; }
```

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

* class [ChartTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
