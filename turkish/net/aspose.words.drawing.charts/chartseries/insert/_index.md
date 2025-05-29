---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: .NET için Aspose.Words
description: ChartSeries Ekleme yöntemiyle grafiklerinizi zahmetsizce geliştirin. Herhangi bir endekse X değerleri ekleyin, veri görselleştirmenizi kolaylıkla optimize edin!
type: docs
weight: 200
url: /tr/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

Belirtilen X değerini belirtilen dizindeki grafik serisine ekler. Seri Y değerlerini ve kabarcık boyutlarını destekliyorsa, X değeri için boş olacaklardır.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## Notlar

Varsayılan biçimlendirmeye sahip karşılık gelen veri noktası veri noktası koleksiyonuna eklenecektir. Ve, veri etiketleri görüntüleniyorsa, varsayılan biçimlendirmeye sahip karşılık gelen veri etiketi de eklenecektir.

## Örnekler

Bir grafik serisine verinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();
// Seriyi verilerle doldur.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

Belirtilen X ve Y değerlerini belirtilen dizindeki grafik serisine ekler.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## Notlar

Varsayılan biçimlendirmeye sahip karşılık gelen veri noktası veri noktası koleksiyonuna eklenecektir. Ve, veri etiketleri görüntüleniyorsa, varsayılan biçimlendirmeye sahip karşılık gelen veri etiketi de eklenecektir.

## Örnekler

Bir grafik serisine verinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();
// Seriyi verilerle doldur.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

Belirtilen X değerini, Y değerini ve kabarcık boyutunu belirtilen dizindeki grafik serisine ekler.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Notlar

Varsayılan biçimlendirmeye sahip karşılık gelen veri noktası veri noktası koleksiyonuna eklenecektir. Ve, veri etiketleri görüntüleniyorsa, varsayılan biçimlendirmeye sahip karşılık gelen veri etiketi de eklenecektir.

## Örnekler

Bir grafik serisine verinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();
// Seriyi verilerle doldur.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
