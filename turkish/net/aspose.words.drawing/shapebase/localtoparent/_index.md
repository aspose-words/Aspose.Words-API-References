---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: .NET için Aspose.Words
description: ShapeBase LocalToParent yöntemi ile yerel koordinatları ana şekil alanına dönüştürün. 3B modelleme projelerinizde hassasiyeti bugün artırın!
type: docs
weight: 680
url: /tr/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Yerel koordinat alanındaki bir değeri ana şeklin koordinat alanına dönüştürür.

```csharp
public PointF LocalToParent(PointF value)
```

## Örnekler

Bir şeklin koordinat düzlemindeki x ve y koordinat konumunun, ana şeklin koordinat düzlemindeki bir konuma nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();

// Bir grup şekli ekleyin ve onu 100 puan aşağı ve sağına yerleştirin
// belgenin x ve Y koordinatlarındaki başlangıç noktası.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Grubun dahili x ve y koordinatlarında (0, 0) olduğunu belirlemek için "LocalToParent" yöntemini kullanın
// ebeveyn şeklinin koordinat sisteminin (100, 100) noktasında yer alır. Grup şeklinin ebeveyni belgenin kendisidir.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Varsayılan olarak, bir şeklin dahili koordinat düzleminin sol üst köşesi (0, 0) konumundadır,
// ve sağ alt köşede (1000, 1000). Boyutu nedeniyle, grup şeklimiz 500pt x 500pt'lik bir alanı kaplar
// belgenin düzleminde. Bu, belgenin koordinat düzleminde 1pt'lik bir hareketin çevrileceği anlamına gelir
// grup şeklinin koordinat düzleminde 2pt'lik bir harekete.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Grup şeklinin x ve y eksenlerinin başlangıcını sol üst köşeden merkeze taşı.
// Bu, grubun iç koordinatlarını belgenin koordinatlarına göre daha da kaydıracaktır.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Koordinat düzleminin ölçeğinin değiştirilmesi, göreceli konumları da etkileyecektir.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Belgedeki bir konuma göre konumunu tanımlayarak bu gruba bir şekil eklemek istersek,
// Öncelikle belgenin konumuyla eşleşecek grup şeklindeki bir konumu onaylamamız gerekecek.
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
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
