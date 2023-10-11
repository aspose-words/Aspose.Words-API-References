---
title: ChartXValue.FromString
second_title: Aspose.Words per .NET API Reference
description: ChartXValue metodo. Crea unChartXValue istanza delString tipo.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Crea un[`ChartXValue`](../) istanza delString tipo.

```csharp
public static ChartXValue FromString(string value)
```

### Esempi

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

* class [ChartXValue](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* assemblea [Aspose.Words](../../../)


