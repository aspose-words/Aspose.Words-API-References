---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words per .NET
description: ChartAxis Hidden proprietà. Ottiene o imposta un flag che indica se questo asse è nascosto o meno in C#.
type: docs
weight: 100
url: /it/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Ottiene o imposta un flag che indica se questo asse è nascosto o meno.

```csharp
public bool Hidden { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

## Esempi

Mostra come nascondere gli assi del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Cancella le serie di dati dimostrativi del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiunge una serie personalizzata con categorie per l'asse X e rispettivi valori decimali per l'asse Y.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // Nasconde gli assi del grafico per semplificare l'aspetto del grafico.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Guarda anche

* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
