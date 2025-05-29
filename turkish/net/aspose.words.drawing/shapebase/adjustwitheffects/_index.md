---
title: ShapeBase.AdjustWithEffects
linktitle: AdjustWithEffects
articleTitle: AdjustWithEffects
second_title: .NET için Aspose.Words
description: ShapeBase AdjustWithEffects yönteminin efekt kapsamları ekleyerek kaynak dikdörtgeninizi nasıl geliştirdiğini ve kesin son dikdörtgen değerleri sağladığını keşfedin.
type: docs
weight: 660
url: /tr/net/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method

Kaynak dikdörtgene efekt kapsamının değerlerini ekler ve son dikdörtgeni döndürür.

```csharp
public RectangleF AdjustWithEffects(RectangleF source)
```

## Örnekler

Bir şeklin sınırlarının şekil etkilerinden nasıl etkilendiğinin nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// İki şekil de boyut ve şekil türü açısından aynıdır.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// İlk şeklin hiçbir efekti yok, ikincisinin ise gölgesi ve kalın bir dış çizgisi var.
// Bu efektler ikinci şeklin silüetinin boyutunu birinciden daha büyük yapar.
// Microsoft Word'de bu şekillere tıkladığımızda dikdörtgenin boyutu görünse de,
// İkinci şeklin görünen dış sınırları gölge ve anahattan etkilendiği için daha büyüktür.
// Şeklin gerçek boyutunu görmek için "AdjustWithEffects" metodunu kullanabiliriz.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// Bir dikdörtgeni temsil eden bir RectangleF nesnesi oluşturun,
// bunları potansiyel olarak bir şeklin koordinatları ve sınırları olarak kullanabiliriz.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Tüm şekil efektlerimiz için dikdörtgenin boyutunun ayarlanmasını sağlamak için bu yöntemi çalıştırın.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Şeklin sınır değiştiren bir etkisi olmadığından, sınır boyutları etkilenmez.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// İlk şeklin son boyutunu noktalarla doğrulayın.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Şekil efektleri, şeklin görünen sol üst köşesini biraz hareket ettirdi.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// Etkiler şeklin görünür boyutlarını da etkilemiştir.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1133.5, rectangleFOut.Height);

// Etkiler şeklin görünür sınırlarını da etkiledi.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(280.5, shape.BoundsWithEffects.Height);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
