---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo i valori X, Y e le dimensioni delle bolle dalle tue serie di grafici con il metodo ChartSeries Remove. Semplifica la visualizzazione dei tuoi dati oggi stesso!
type: docs
weight: 210
url: /it/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Rimuove il valore X, il valore Y e la dimensione della bolla, se supportati, dalla serie del grafico all'indice specificato. Vengono rimossi anche il punto dati e l'etichetta dati corrispondenti.

```csharp
public void Remove(int index)
```

## Esempi

Mostra come aggiungere/rimuovere valori dai dati del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Rimuove il primo valore in entrambe le serie.
department1Series.Remove(0);
department2Series.Remove(0);

// Aggiunge nuovi valori ad entrambe le serie.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Guarda anche

* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
