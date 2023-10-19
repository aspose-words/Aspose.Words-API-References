---
title: AxisScaleType Enum
linktitle: AxisScaleType
articleTitle: AxisScaleType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisScaleType Sıralama. Bir eksen için olası ölçek türlerini belirtir C#'da.
type: docs
weight: 560
url: /tr/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

Bir eksen için olası ölçek türlerini belirtir.

```csharp
public enum AxisScaleType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Linear | `0` | Doğrusal ölçeklendirme. |
| Logarithmic | `1` | Logaritmik ölçeklendirme. |

## Örnekler

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
