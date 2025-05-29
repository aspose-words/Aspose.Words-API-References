---
title: AxisScaleType Enum
linktitle: AxisScaleType
articleTitle: AxisScaleType
second_title: .NET için Aspose.Words
description: Grafik deneyiminizi geliştirmek için çok yönlü eksen ölçek türlerini tanımlayan Aspose.Words.Drawing.Charts.AxisScaleType enum'unu keşfedin.
type: docs
weight: 810
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
| Linear | `0` | Doğrusal ölçekleme. |
| Logarithmic | `1` | Logaritmik ölçekleme. |

## Örnekler

Bir grafik eksenine logaritmik ölçeklemenin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Beş nokta için X/Y koordinatlı bir seri ekle.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// X ekseninin ölçeklenmesi varsayılan olarak doğrusaldır,
// X-değer aralığımızı (0, 1, 2, 3...) kapsayan eşit olarak artan değerleri görüntüleme.
// Y değerlerimiz için doğrusal bir eksen ideal değildir
// çünkü Y değeri daha küçük olan noktaların okunması daha zor olacaktır.
// 20 tabanlı logaritmik ölçekleme (1, 20, 400, 8000...)
// çizilen noktaları yayarak, grafikteki değerlerini daha kolay okumamızı sağlayacaktır.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
