---
title: ShapeBase.BoundsInPoints
linktitle: BoundsInPoints
articleTitle: BoundsInPoints
second_title: .NET için Aspose.Words
description: Bir şeklin boyutuna ve konumuna noktalar halinde kolayca erişmek, tasarım hassasiyetinizi ve düzen kontrolünüzü artırmak için ShapeBase BoundsInPoints özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Şeklin içeren bloğunun konumunu ve boyutunu, en üstteki şeklin çapa noktasına göre noktalar halinde alır.

```csharp
public RectangleF BoundsInPoints { get; }
```

## Notlar

Döndürülen sınırlar, varsa bu şeklin dönüşünü veya ana grup şeklinin dönüşünü içermez.

## Örnekler

Blok sınırlarını içeren şeklin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Satırın kendisi belge sayfasında çok az yer kaplamasına rağmen,
// "Bounds" özelliklerini kullanarak boyutunu belirleyebileceğimiz dikdörtgen bir kapsayıcı blok kaplar.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Bir grup şekli oluşturun ve ardından "Bounds" özelliğini kullanarak içeren bloğun boyutunu ayarlayın.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Bir dikdörtgen oluşturun, sınırlayıcı bloğunun boyutunu doğrulayın ve ardından onu grup şekline ekleyin.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Grup şeklinin koordinat düzleminin kökeni, onu içeren bloğun sol üst köşesindedir.
// ve sağ alt köşedeki (1000, 1000) noktasının x ve y koordinatları.
// Grup şeklimiz 250x250pt boyutundadır, bu nedenle grup şeklinin koordinat düzlemindeki her 4pt
// belge gövdesinin koordinat düzleminde 1pt'ye çevrilir.
// Eklediğimiz her şekil aynı zamanda 4 kat küçülecektir.
// Şeklin "BoundsInPoints" özelliğindeki değişiklik bunu yansıtacaktır.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Bir şekil ekle ve onu grup şeklinin bulunduğu bloğun sınırlarının dışına yerleştir.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Grup şeklinin belge gövdesindeki izi arttı, ancak içeren blok aynı kaldı.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
