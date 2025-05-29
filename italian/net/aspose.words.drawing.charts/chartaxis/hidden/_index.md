---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxis Hidden per gestire facilmente la visibilità degli assi nei tuoi grafici. Migliora la presentazione dei tuoi dati con questa semplice funzione di attivazione/disattivazione!
type: docs
weight: 110
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

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiungi una serie personalizzata con categorie per l'asse X e rispettivi valori decimali per l'asse Y.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // Nascondi gli assi del grafico per semplificarne l'aspetto.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Guarda anche

* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
