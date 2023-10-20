---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: ChartSeries Remove metodo. Rimuove il valore X il valore Y e la dimensione della bolla se supportati dalle serie di grafici allindice specificato. Vengono rimossi anche il punto dati e letichetta dati corrispondenti in C#.
type: docs
weight: 200
url: /it/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Rimuove il valore X, il valore Y e la dimensione della bolla, se supportati, dalle serie di grafici all'indice specificato. Vengono rimossi anche il punto dati e l'etichetta dati corrispondenti.

```csharp
public void Remove(int index)
```

## Esempi

Mostra come aggiungere/rimuovere i valori dei dati del grafico.

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

// Aggiunge nuovi valori a entrambe le serie.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Guarda anche

* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
