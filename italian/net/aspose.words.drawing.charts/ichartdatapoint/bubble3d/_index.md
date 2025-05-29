---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words per .NET
description: Scopri la proprietà Bubble3D di IChartDataPoint per migliorare i tuoi grafici a bolle con straordinari effetti 3D per una visualizzazione dei dati più coinvolgente.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Specifica se alle bolle nel grafico a bolle deve essere applicato un effetto 3D.

```csharp
public bool Bubble3D { get; set; }
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

// Applica un'etichetta dati a ciascuna bolla che ne visualizza il diametro.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Guarda anche

* interface [IChartDataPoint](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
