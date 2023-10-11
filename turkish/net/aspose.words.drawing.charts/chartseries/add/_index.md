---
title: ChartSeries.Add
second_title: Aspose.Words for .NET API Referansı
description: ChartSeries yöntem. Belirtilen X değerini grafik serisine ekler. Seri Y değerlerini ve kabarcık boyutlarını destekliyorsa bunlar X değeri için boş olacaktır.
type: docs
weight: 160
url: /tr/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(ChartXValue) {#add}

Belirtilen X değerini grafik serisine ekler. Seri, Y değerlerini ve kabarcık boyutlarını destekliyorsa, bunlar X değeri için boş olacaktır.

```csharp
public void Add(ChartXValue xValue)
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseries/)
* toplantı [Aspose.Words](../../../)

---

## Add(ChartXValue, ChartYValue) {#add_1}

Belirtilen X ve Y değerlerini grafik serisine ekler.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
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

Grafik serisinin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();

// Seriyi verilerle dolduruyoruz.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// İkinci serinin X ve Y değerlerini temizle.
series2.ClearValues();

// Seriyi verilerle dolduruyoruz.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseries/)
* toplantı [Aspose.Words](../../../)

---

## Add(ChartXValue, ChartYValue, double) {#add_2}

Belirtilen X değerini, Y değerini ve kabarcık boyutunu grafik serisine ekler.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseries/)
* toplantı [Aspose.Words](../../../)


