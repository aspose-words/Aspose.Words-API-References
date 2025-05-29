---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words per .NET
description: Scopri se un formato è definito con la proprietà ChartFormat IsDefined. Ottieni subito un controllo impeccabile sulla formattazione dei tuoi grafici!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Ottiene un flag che indica se è definito un formato.

```csharp
public bool IsDefined { get; }
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
