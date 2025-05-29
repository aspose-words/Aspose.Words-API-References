---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: .NET için Aspose.Words
description: Optimum okunabilirlik için AxisTickLabels yönlendirmenizi özelleştirin. Veri görselleştirmenizi geliştirmek için kolayca tick etiket metni yönünü ayarlayın!
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

İşaret etiketi metninin yönünü alır veya ayarlar.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Notlar

Varsayılan değer:Horizontal.

Bazılarının şunu unutmayın[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) değerler, değer eksenlerindeki text onay etiketinin yönünü etkilemez.

## Örnekler

Eksen işareti etiketleri için yönelim ve dönüşün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sütun grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Eksen işaretinin etiket yönünü ve dönüşünü ayarlayın.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Ayrıca bakınız

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
