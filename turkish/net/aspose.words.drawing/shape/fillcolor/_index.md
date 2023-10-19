---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words for .NET
description: Shape FillColor mülk. Şeklin kapalı yolunu dolduran fırça rengini tanımlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Şeklin kapalı yolunu dolduran fırça rengini tanımlar.

```csharp
public Color FillColor { get; set; }
```

## Notlar

Bu, kısayol[`Color`](../../fill/color/) mülk.

Varsayılan değer: White.

## Örnekler

Bir şeklin düz renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir miktar metin yazın ve ardından onu kayan bir şekille kaplayın.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin anahattının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opaklık" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak ve 0 görünmez olacak şekilde.
// Şekil dolgusu varsayılan olarak tamamen opaktır, dolayısıyla bu şeklin üstünde olduğu metni göremiyoruz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Şekil dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ayrıca bakınız

* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
