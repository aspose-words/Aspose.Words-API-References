---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo ChartFormat SetDefaultFill per ripristinare senza sforzo il riempimento di un elemento del grafico al suo valore predefinito originale.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Reimposta il riempimento dell'elemento del grafico in modo che abbia il valore predefinito.

```csharp
public void SetDefaultFill()
```

## Esempi

Mostra come reimpostare il riempimento al valore predefinito definito nella serie.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Guarda anche

* class [ChartFormat](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
