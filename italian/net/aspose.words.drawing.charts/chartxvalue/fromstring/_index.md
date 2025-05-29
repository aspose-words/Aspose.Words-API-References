---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words per .NET
description: Scopri il metodo ChartXValue FromString per creare facilmente istanze di ChartXValue di tipo String. Migliora la tua visualizzazione dati oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Crea un[`ChartXValue`](../) istanza delString tipo.

```csharp
public static ChartXValue FromString(string value)
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

* class [ChartXValue](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
