---
title: ShapeBase.LocalToParent
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase yöntem. Yerel koordinat alanından bir değeri ana şeklin koordinat alanına dönüştürür.
type: docs
weight: 610
url: /tr/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Yerel koordinat alanından bir değeri ana şeklin koordinat alanına dönüştürür.

```csharp
public PointF LocalToParent(PointF value)
```

### Örnekler

Bir şeklin koordinat düzlemindeki x ve y koordinat konumunun üst şeklin koordinat düzlemindeki bir konuma nasıl çevrileceğini gösterir.

```csharp
Document doc = new Document();

// Bir grup şekli ekleyin ve onu 100 puan aşağı ve sağına yerleştirin.
// belgenin x ve Y koordinat başlangıç noktası.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Grubun dahili x ve y koordinatlarında (0, 0) olduğunu belirlemek için "LocalToParent" yöntemini kullanın
// üst şeklinin koordinat sisteminin (100, 100) üzerinde bulunur. Grup şeklinin ebeveyni belgenin kendisidir.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Varsayılan olarak, bir şeklin iç koordinat düzleminin sol üst köşesi (0, 0),
// ve sağ alt köşede (1000, 1000). Büyüklüğü nedeniyle grup şeklimiz 500pt x 500pt'lik bir alanı kaplamaktadır.
// belgenin düzleminde. Bu, belgenin koordinat düzleminde 1pt'lik bir hareketin çevrileceği anlamına gelir.
// grup şeklinin koordinat düzleminde 2 puntoluk bir harekete.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Grup şeklinin x ve y ekseni orijinini sol üst köşeden merkeze taşıyın.
// Bu, grubun dahili koordinatlarını belgenin koordinatlarına göre daha da öteler.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Koordinat düzleminin ölçeğini değiştirmek, göreli konumları da etkiler.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Bu gruba bir şekil eklemek istersek, dökümandaki bir lokasyona göre lokasyonunu tanımlarken,
// önce grup şeklindeki belgenin konumuyla eşleşen bir konumu onaylamamız gerekecek.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


