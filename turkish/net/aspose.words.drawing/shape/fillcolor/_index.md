---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: .NET için Aspose.Words
description: Şekillerinizi geliştiren ve projelerinizi bir üst seviyeye taşıyan canlı fırça renkleriyle tasarımlarınızı özelleştirmek için Shape FillColor özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Şeklin kapalı yolunu dolduran fırça rengini tanımlar.

```csharp
public Color FillColor { get; set; }
```

## Notlar

Bu, şuna giden bir kısayoldur:[`Color`](../../fill/color/) mülk.

Varsayılan değer White .

## Örnekler

Bir şeklin düz bir renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Biraz metin yazın ve ardından onu yüzen bir şekille örtün.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin dış hatlarının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opaklık" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak, 0 ise görünmez anlamına gelir.
// Şeklin dolgusu varsayılan olarak tamamen opak olduğundan, şeklin üstündeki metni göremeyiz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Şeklin dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ayrıca bakınız

* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
