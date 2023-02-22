---
title: ShapeBase.DistanceTop
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Belge metni ile şeklin üst kenarı arasındaki mesafeyi nokta olarak döndürür veya ayarlar.
type: docs
weight: 160
url: /tr/net/aspose.words.drawing/shapebase/distancetop/
---
## ShapeBase.DistanceTop property

Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta olarak) döndürür veya ayarlar.

```csharp
public double DistanceTop { get; set; }
```

### Notlar

Varsayılan değer 0'dır.

Yalnızca üst düzey şekiller için etkilidir.

### Örnekler

Bir şekli çevreleyen bir metin için sarma mesafesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir dikdörtgen ekleyin ve metnin sınırlarını sıkıca sarmasını sağlayın.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Şekil ile çevreleyen metin arasındaki minimum mesafeyi her taraftan 40pt olarak ayarlayın.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Şekli sayfanın ortasına yaklaştırın ve ardından şekli saat yönünde 60 derece döndürün.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// Şekli saracak metin ekleyin.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


