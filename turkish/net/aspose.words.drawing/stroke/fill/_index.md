---
title: Stroke.Fill
linktitle: Fill
articleTitle: Fill
second_title: .NET için Aspose.Words
description: Tasarımlarınızda gelişmiş dolgu biçimlendirmesi için Stroke Fill özelliğini keşfedin. Bugün hassas vuruş özelleştirmesiyle projelerinizi yükseltin!
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/stroke/fill/
---
## Stroke.Fill property

için doldurma biçimlendirmesini alır[`Stroke`](../) .

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../fill/)
* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
