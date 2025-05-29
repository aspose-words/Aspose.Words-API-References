---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: .NET için Aspose.Words
description: Şekiller için fırça kalınlığını özelleştirmek üzere Stroke Weight özelliğini keşfedin. Tasarımlarınızı noktalardaki hassas yol vuruşlarıyla geliştirin!
type: docs
weight: 260
url: /tr/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

Bir şeklin yolunu noktalar halinde çizen fırça kalınlığını tanımlar.

```csharp
public double Weight { get; set; }
```

## Notlar

Bir için varsayılan değer[`Shape`](../../shape/) 0,75'tir.

## Örnekler

Vuruş özelliklerinin nasıl değiştiğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Dikdörtgen gibi temel şekillerin iki görünür kısmı vardır.
// 1 - Şeklin dış hatları içindeki alana uygulanan dolgu:
shape.Fill.ForeColor = Color.White;

// 2 - Şeklin ana hatlarını belirleyen çizgi:
// Bu şeklin konturunun çeşitli özelliklerini değiştirin.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
