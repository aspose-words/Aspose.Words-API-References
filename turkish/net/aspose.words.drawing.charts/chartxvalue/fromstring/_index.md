---
title: ChartXValue.FromString
second_title: Aspose.Words for .NET API Referansı
description: ChartXValue yöntem. Bir oluştururChartXValue örneğiString type.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Bir oluşturur[`ChartXValue`](../) örneğiString type.

```csharp
public static ChartXValue FromString(string value)
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

* class [ChartXValue](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* toplantı [Aspose.Words](../../../)


