---
title: Stroke.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: .NET için Aspose.Words
description: Projenizin görsel çekiciliğini artırmak için benzersiz çizgi stilleriyle tasarımınızı özelleştirmek üzere Stroke LineStyle özelliğini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words.drawing/stroke/linestyle/
---
## Stroke.LineStyle property

Konturun çizgi stilini tanımlar.

```csharp
public ShapeLineStyle LineStyle { get; set; }
```

## Notlar

Varsayılan değer:Single.

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

* enum [ShapeLineStyle](../../shapelinestyle/)
* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
