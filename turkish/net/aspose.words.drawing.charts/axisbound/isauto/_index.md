---
title: AxisBound.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: .NET için Aspose.Words
description: AxisBound IsAuto'yu keşfedin. Gelişmiş veri görselleştirme ve akıcı analiz için eksen sınırlarını otomatik olarak belirleyin. Grafiklerinizi zahmetsizce optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/axisbound/isauto/
---
## AxisBound.IsAuto property

Eksen sınırının otomatik olarak belirlenmesi gerektiğini belirten bir bayrak döndürür.

```csharp
public bool IsAuto { get; }
```

## Örnekler

Özel eksen sınırlarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// İki ondalık diziden oluşan bir seri ekleyin. İlk dizi X değerlerini içerir,
// ve ikincisi dağılım grafiğindeki noktalara karşılık gelen Y değerlerini içerir.
chart.Series.Add("Series 1",
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 },
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Varsayılan olarak, varsayılan ölçekleme grafiğin X ve Y eksenlerine uygulanır,
// böylece her ikisinin de aralıkları her serinin her X ve Y değerini kapsayacak kadar büyük olur.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Kendi eksen sınırlarımızı tanımlayabiliriz.
// Bu durumda hem X hem de Y ekseni cetvellerinin 0 ile 10 arasında bir aralık göstermesini sağlayacağız.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// X ekseninde bir tarih aralığı ve Y ekseninde ondalık değerler gerektiren bir seri içeren bir çizgi grafiği oluşturun.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// Eksen sınırlarını tarih biçiminde de belirleyebilir, grafiği bir döneme sınırlayabiliriz.
// Aralığı 1980-1990 olarak ayarlamak, serinin iki değerini atlayacaktır
// grafik aralığının dışında kalanlar.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Ayrıca bakınız

* class [AxisBound](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
