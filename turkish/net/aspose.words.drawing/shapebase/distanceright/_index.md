---
title: ShapeBase.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: .NET için Aspose.Words
description: ShapeBase DistanceRight özelliğini keşfedin, gelişmiş düzen kontrolü için belge metniniz ile şeklin sağ kenarı arasındaki nokta aralıklarını kolayca ayarlayın.
type: docs
weight: 150
url: /tr/net/aspose.words.drawing/shapebase/distanceright/
---
## ShapeBase.DistanceRight property

Belge metni ile şeklin sağ kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double DistanceRight { get; set; }
```

## Notlar

Varsayılan değer 1/8 inçtir.

Sadece en üst seviye şekiller için etkilidir.

## Örnekler

Bir şekli çevreleyen metin için kaydırma mesafesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir dikdörtgen ekleyin ve metnin dikdörtgenin sınırları etrafında sıkıca sarılmasını sağlayın.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Şekil ile çevresindeki metin arasındaki minimum mesafeyi her taraftan 40pt olarak ayarlayın.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Şekli sayfanın ortasına yaklaştırın ve ardından şekli saat yönünde 60 derece döndürün.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

// Şeklin etrafını saracak metni ekle.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
