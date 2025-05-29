---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words per .NET
description: Scopri il metodo ChartSeries CopyFormatFrom per replicare senza sforzo i formati dei punti dati tramite indice, migliorando l'efficienza e la coerenza dei tuoi grafici.
type: docs
weight: 190
url: /it/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

Copia il formato predefinito del punto dati dal punto dati con l'indice specificato.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## Esempi

Mostra come copiare il formato dei punti dati.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Ottieni il grafico e la serie per aggiornare il formato.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// Copia il formato del punto dati con indice 1 nel punto dati con indice 2
// in modo che il punto dati 2 sia uguale al punto dati 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// Copia il formato del punto dati con indice 0 nei valori predefiniti della serie in modo che tutti i punti dati
// nella serie che ha il formato predefinito hanno lo stesso aspetto del punto dati 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Guarda anche

* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
