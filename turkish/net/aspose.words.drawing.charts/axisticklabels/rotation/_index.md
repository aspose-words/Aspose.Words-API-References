---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: .NET için Aspose.Words
description: En iyi okunabilirlik için AxisTickLabels dönüşünü ayarlayın. Grafiğinizin netliğini ve görsel çekiciliğini artırmak için etiket açılarını derece cinsinden özelleştirin.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Tik etiketlerinin derece cinsinden dönüşünü alır veya ayarlar.

```csharp
public int Rotation { get; set; }
```

## Notlar

Kabul edilebilir değerler aralığı -180 ile 180 dahil arasındadır. Varsayılan değer 0'dır.

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

* class [AxisTickLabels](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
