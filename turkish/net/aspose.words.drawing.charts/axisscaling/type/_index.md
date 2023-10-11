---
title: AxisScaling.Type
second_title: Aspose.Words for .NET API Referansı
description: AxisScaling mülk. Eksenin ölçeklendirme türünü alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

Eksenin ölçeklendirme türünü alır veya ayarlar.

```csharp
public AxisScaleType Type { get; set; }
```

### Notlar

Linear MS Office 2016 yeni grafiklerinde izin verilen tek değerdir.

### Örnekler

Logaritmik ölçeklendirmenin bir grafik eksenine nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Beş nokta için X/Y koordinatlarına sahip bir seri ekleyin.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// X ekseninin ölçeklendirmesi varsayılan olarak doğrusaldır,
// X değeri aralığımızı (0, 1, 2, 3...) kapsayan eşit şekilde artan değerleri gösteriyoruz.
// Y değerlerimiz için doğrusal bir eksen ideal değildir
// çünkü Y değeri daha küçük olan noktaların okunması daha zor olacaktır.
// 20 (1, 20, 400, 8000...) tabanlı logaritmik ölçeklendirme
// çizilen noktaları yayarak değerlerini grafik üzerinde daha kolay okumamızı sağlayacak.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Ayrıca bakınız

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../axisscaling/)
* toplantı [Aspose.Words](../../../)


