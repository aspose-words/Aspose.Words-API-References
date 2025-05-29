---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: Grafiklerinize X değerlerini kolayca entegre etmek için ChartSeries Add yöntemini keşfedin. Y değerleri ve kabarcık boyutları desteğiyle veri görselleştirmeyi geliştirin.
type: docs
weight: 160
url: /tr/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Belirtilen X değerini grafik serisine ekler. Seri Y değerlerini ve baloncuk boyutlarını destekliyorsa, X değeri için boş olacaklardır.

```csharp
public void Add(ChartXValue xValue)
```

## Örnekler

Grafik serilerinin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();

// Seriyi verilerle doldur.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// İkinci serinin X ve Y değerlerini temizle.
series2.Clear();

// Seriyi verilerle doldur.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Belirtilen X ve Y değerlerini grafik serisine ekler.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
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

Grafik serilerinin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();

// Seriyi verilerle doldur.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// İkinci serinin X ve Y değerlerini temizle.
series2.Clear();

// Seriyi verilerle doldur.
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
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Grafik serisine belirtilen X değerini, Y değerini ve kabarcık boyutunu ekler.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Örnekler

Grafik serilerinin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();

// Seriyi verilerle doldur.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// İkinci serinin X ve Y değerlerini temizle.
series2.Clear();

// Seriyi verilerle doldur.
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
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
