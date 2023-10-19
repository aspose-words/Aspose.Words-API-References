---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words for .NET
description: ShapeBase LocalToParent yöntem. Yerel koordinat alanından bir değeri üst şeklin koordinat alanına dönüştürür C#'da.
type: docs
weight: 670
url: /tr/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Yerel koordinat alanından bir değeri üst şeklin koordinat alanına dönüştürür.

```csharp
public PointF LocalToParent(PointF value)
```

## Örnekler

Bir şeklin koordinat düzlemindeki x ve y koordinat konumunun üst şeklin koordinat düzlemindeki bir konuma nasıl çevrileceğini gösterir.

```csharp
Document doc = new Document();

// Bir grup şekli ekleyin ve onu 100 puan aşağıya ve sağına yerleştirin
// belgenin x ve Y koordinatı başlangıç noktası.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Grubun dahili x ve y koordinatlarında (0, 0) olduğunu belirlemek için "LocalToParent" yöntemini kullanın
// ana şeklin koordinat sisteminin (100, 100) üzerinde yer alır. Grup şeklinin üst öğesi belgenin kendisidir.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Varsayılan olarak, bir şeklin iç koordinat düzleminin sol üst köşesi (0, 0)'dadır,
// ve sağ alt köşede (1000, 1000). Büyüklüğü nedeniyle grup şeklimiz 500pt x 500pt alanı kaplamaktadır.
// belgenin düzleminde. Bu, belgenin koordinat düzleminde 1 puntoluk bir hareketin tercüme edileceği anlamına gelir
// grup şeklinin koordinat düzleminde 2 puanlık bir harekete.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Grup şeklinin x ve y eksenini sol üst köşeden merkeze taşıyın.
// Bu, grubun iç koordinatlarını belgenin koordinatlarına göre daha da fazla kaydıracaktır.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Koordinat düzleminin ölçeğinin değiştirilmesi göreceli konumları da etkileyecektir.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Bu gruba belgedeki bir konuma göre konumunu tanımlarken bir şekil eklemek istersek,
// öncelikle grup şeklinde belgenin konumuyla eşleşecek bir konumu onaylamamız gerekecek.
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
