---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: .NET için Aspose.Words
description: Şeklinizin metinle hizalanıp hizalanmadığını kolayca kontrol etmek, tasarımınızı geliştirmek ve düzen verimliliğini artırmak için ShapeBase IsInline özelliğini keşfedin.
type: docs
weight: 310
url: /tr/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Bu şeklin metinle aynı hizada konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu.

```csharp
public bool IsInline { get; }
```

## Notlar

Sadece en üst seviye şekiller için etkilidir.

## Örnekler

Bir şeklin satır içi mi yoksa yüzen mi olduğunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Satır içi:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Satır içi şekil, metin parçaları gibi diğer paragraf öğelerinin arasında bir paragrafın içinde yer alır.
// Microsoft Word'de şekli bir karaktermiş gibi tıklayıp istediğimiz paragrafa sürükleyebiliriz.
// Şekil büyükse dikey paragraf aralığı etkilenir.
// Bu şekli paragraf olmayan bir yere taşıyamayız.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Yüzen:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Yüzen bir şekil, onu eklediğimiz paragrafa aittir,
// Şeklin üzerine tıkladığımızda çıkan bir bağlantı sembolünden bunu belirleyebiliriz.
// Şeklin solunda görünür bir bağlantı sembolü yoksa,
// "Seçenekler" -> "Görüntüle" -> "Nesne Bağlantı Noktaları" yoluyla görünür bağlantıları etkinleştirmemiz gerekecek.
// Microsoft Word'de bu şeklin üzerine sol tıklayıp istediğimiz yere sürükleyebiliriz.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
