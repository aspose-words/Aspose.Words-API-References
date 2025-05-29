---
title: ChartDataPointCollection.CopyFormat
linktitle: CopyFormat
articleTitle: CopyFormat
second_title: Aspose.Words per .NET
description: Copia senza sforzo la formattazione tra i punti dati con il metodo ChartDataPointCollection CopyFormat. Migliora la visualizzazione dei tuoi dati oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection.CopyFormat method

Copia il formato dal punto dati di origine al punto dati di destinazione.

```csharp
public void CopyFormat(int sourceIndex, int destinationIndex)
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

* class [ChartDataPointCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
