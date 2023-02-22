---
title: Fill.Opacity
second_title: Aspose.Words for .NET API Referansı
description: Fill mülk. Belirtilen dolgunun opaklık derecesini 0.0 net ile 1.0 opak arasında bir değer olarak alır veya ayarlar.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Belirtilen dolgunun opaklık derecesini 0.0 (net) ile 1.0 (opak) arasında bir değer olarak alır veya ayarlar.

```csharp
public double Opacity { get; set; }
```

### Notlar

Bu özellik, mülkün tam tersidir.[`Transparency`](../transparency/).

### Örnekler

Bir şeklin düz bir renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir metin yazın ve ardından kayan bir şekille kaplayın.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin anahattının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opacity" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak ve 0 görünmez olmak üzere.
// Şekil dolgusu varsayılan olarak tamamen opaktır, bu nedenle bu şeklin üzerinde olduğu metni göremeyiz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Altındaki metni görebilmemiz için şekil dolgu renginin opaklığını daha düşük bir değere ayarlayın.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)


