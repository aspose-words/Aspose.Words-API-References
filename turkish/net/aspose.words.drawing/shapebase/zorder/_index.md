---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: .NET için Aspose.Words
description: ShapeBase ZOrder özelliğinin, daha net ve daha düzenli bir düzen için üst üste binen şekillerin görüntülenme sırasını kontrol ederek tasarımınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 650
url: /tr/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Çakışan şekillerin görüntülenme sırasını belirler.

```csharp
public int ZOrder { get; set; }
```

## Notlar

Sadece en üst seviye şekiller için etkilidir.

Varsayılan değer 0'dır.

Sayı, istifleme önceliğini temsil eder. Daha yüksek sayıya sahip bir şekil, daha düşük sayıya sahip bir şeklin "önünde"ymiş gibi görüntülenecektir.

Örtüşen şekillerin sırası, başlıktaki şekiller ve belgenin main metnindeki şekiller için bağımsızdır.

Bir grup şeklindeki çocuk şekillerin görüntülenme sırası, grup şekli içindeki order ile belirlenir.

## Örnekler

Şekillerin sırasının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Birbirinin kısmen üst üste binen üç farklı renkli dikdörtgen ekleyin.
// Başka bir şeklin üzerine gelecek şekilde yeni bir şekil eklediğimizde, Aspose.Words yeni şekli eskisinin üstüne yerleştirir.
// Açık yeşil dikdörtgen açık mavi dikdörtgenin üzerine gelecek ve onu kısmen kapatacaktır.
// ve açık mavi dikdörtgen turuncu dikdörtgeni gizleyecektir.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// Bir şeklin "ZOrder" özelliği, diğer örtüşen şekiller arasındaki istifleme önceliğini belirler.
// Eğer iki örtüşen şeklin farklı "ZOrder" değerleri varsa,
 // Microsoft Word, daha yüksek değere sahip şekli, daha düşük değere sahip şeklin üstüne yerleştirecektir.
// Şekillerimizin "ZOrder" değerlerini, ilk turuncu dikdörtgeni ikinci açık mavi dikdörtgenin üzerine yerleştirecek şekilde ayarlayın
// ve üçüncü açık yeşil dikdörtgenin üstündeki ikinci açık mavi dikdörtgen.
// Bu, orijinal yığınlama sırasını tersine çevirecektir.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
