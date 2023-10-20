---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: ChartDataLabel Font proprietà. Fornisce laccesso alla formattazione dei caratteri di questa etichetta dati in C#.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Fornisce l'accesso alla formattazione dei caratteri di questa etichetta dati.

```csharp
public Font Font { get; }
```

## Esempi

Mostra come utilizzare gli effetti 3D con i grafici a bolle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Applica un'etichetta dati a ciascuna bolla che ne mostra il diametro.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Guarda anche

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
