---
title: Fill.Opacity
linktitle: Opacity
articleTitle: Opacity
second_title: .NET için Aspose.Words
description: Tasarımınızın şeffaflığını Fill Opacity özelliğiyle kontrol edin; çarpıcı görseller için netliği tamamen şeffaftan tamamen opaklığa ayarlayın.
type: docs
weight: 150
url: /tr/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Belirtilen dolgunun opaklık derecesini 0,0 (temiz) ile 1,0 (opak) arasında bir değer olarak alır veya ayarlar.

```csharp
public double Opacity { get; set; }
```

## Notlar

Bu özellik, özelliğin tam tersidir[`Transparency`](../transparency/).

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

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
