---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: .NET için Aspose.Words
description: String türünde ChartXValue örnekleri oluşturmak için ChartXValue FromString metodunu keşfedin. Veri görselleştirmenizi bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Bir tane oluşturur[`ChartXValue`](../) örneğiString tür.

```csharp
public static ChartXValue FromString(string value)
```

## Örnekler

Grafik veri değerlerinin nasıl ekleneceğini/kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Her iki serideki ilk değeri kaldır.
department1Series.Remove(0);
department2Series.Remove(0);

// Her iki seriye de yeni değerler ekleyin.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Ayrıca bakınız

* class [ChartXValue](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
