---
title: Stroke.On
linktitle: On
articleTitle: On
second_title: .NET için Aspose.Words
description: Stroke On özelliğiyle yol stilini kontrol edin. Cilalı, profesyonel bir görünüm için yolların nasıl çizileceğini tanımlayarak tasarımlarınızı geliştirin.
type: docs
weight: 190
url: /tr/net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

Yolun çizilip çizilmeyeceğini tanımlar.

```csharp
public bool On { get; set; }
```

## Notlar

Bir için varsayılan değer[`Shape`](../../shape/) dır`doğru`.

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
