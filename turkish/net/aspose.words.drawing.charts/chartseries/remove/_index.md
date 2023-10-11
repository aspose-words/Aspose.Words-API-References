---
title: ChartSeries.Remove
second_title: Aspose.Words for .NET API Referansı
description: ChartSeries yöntem. Belirtilen dizindeki grafik serisinden X değerini Y değerini ve kabarcık boyutunu destekleniyorsa kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır.
type: docs
weight: 210
url: /tr/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Belirtilen dizindeki grafik serisinden X değerini, Y değerini ve kabarcık boyutunu (destekleniyorsa) kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır.

```csharp
public void Remove(int index)
```

### Örnekler

Grafik veri değerlerinin nasıl ekleneceğini/kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Her iki serideki ilk değeri kaldırın.
department1Series.Remove(0);
department2Series.Remove(0);

// Her iki seriye de yeni değerler ekliyoruz.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Ayrıca bakınız

* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseries/)
* toplantı [Aspose.Words](../../../)


