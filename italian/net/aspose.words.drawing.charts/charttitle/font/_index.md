---
title: ChartTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: Personalizza il titolo del grafico con la proprietà Carattere ChartTitle per una formattazione migliorata. Migliora la presentazione dei tuoi dati senza sforzo!
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/charttitle/font/
---
## ChartTitle.Font property

Fornisce accesso alla formattazione del carattere del titolo del grafico.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
