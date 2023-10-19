---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words for .NET
description: ShapeBase ZOrder mülk. Çakışan şekillerin görüntülenme sırasını belirler C#'da.
type: docs
weight: 610
url: /tr/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Çakışan şekillerin görüntülenme sırasını belirler.

```csharp
public int ZOrder { get; set; }
```

## Notlar

Yalnızca üst düzey şekiller için etkilidir.

Varsayılan değer 0'dır.

Sayı istifleme önceliğini temsil eder. Daha yüksek sayıya sahip bir şekil, sanki daha düşük sayıya sahip bir şeklin ("önünde") üst üste binmiş gibi görüntülenecektir .

Çakışan şekillerin sırası, başlıktaki ve belgenin main metnindeki şekillerden bağımsızdır.

Bir grup şeklindeki alt şekillerin görüntülenme sırası, grup şekli içindeki order ile belirlenir.

## Örnekler

Şekillerin sırasının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kısmen birbiriyle örtüşen üç farklı renkli dikdörtgen ekleyin.
// Başka bir şeklin üzerine binen bir şekil eklediğimizde Aspose.Words yeni şekli eski şeklin üzerine yerleştirir.
// Açık yeşil dikdörtgen, açık mavi dikdörtgenin üzerine binecek ve onu kısmen gizleyecektir,
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

// Bir şeklin "ZOrder" özelliği, onun diğer örtüşen şekiller arasında istiflenme önceliğini belirler.
// Üst üste binen iki şeklin farklı "ZOrder" değerleri varsa,
// Microsoft Word, değeri yüksek olan şekli, değeri düşük olan şeklin üzerine yerleştirecektir. 
// Şekillerimizin "ZOrder" değerlerini, ilk turuncu dikdörtgeni ikinci açık mavi dikdörtgenin üzerine yerleştirecek şekilde ayarlayın
// ve üçüncü açık yeşil dikdörtgenin üzerindeki ikinci açık mavi dikdörtgen.
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
