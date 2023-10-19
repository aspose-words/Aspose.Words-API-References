---
title: ShapeBase.CoordOrigin
linktitle: CoordOrigin
articleTitle: CoordOrigin
second_title: Aspose.Words for .NET
description: ShapeBase CoordOrigin mülk. Bu şeklin bulunduğu bloğun sol üst köşesindeki koordinatlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Bu şeklin bulunduğu bloğun sol üst köşesindeki koordinatlar.

```csharp
public Point CoordOrigin { get; set; }
```

## Notlar

Varsayılan değer (0,0)'dır.

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

Grup şeklinin nasıl oluşturulacağını ve doldurulacağını gösterir.

```csharp
Document doc = new Document();

// Bir grup şekli oluşturun. Bir grup şekli, alt şekil düğümlerinin bir koleksiyonunu görüntüleyebilir.
// Microsoft Word'de grup şeklinin sınırları içine veya grup şeklinin alt şekillerinden birine tıklamak
// bu gruptaki diğer tüm alt şekilleri seçin ve tüm şekilleri aynı anda ölçeklendirmemize ve taşımamıza izin verin.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// 400pt x 400pt'lik bir grup şekli oluşturun ve bunu belgenin kayan şekil koordinat kökenine yerleştirin.
group.Bounds = new RectangleF(0, 0, 400, 400);

// Grubun dahili koordinat düzlemi boyutunu 500 x 500 punto olarak ayarlayın. 
// Grubun sol üst köşesi (0, 0) x ve y koordinatına sahip olacaktır,
// ve sağ alt köşede (500, 500) x ve y koordinatları olacaktır.
group.CoordSize = new Size(500, 500);

// Grubun sol üst köşesinin koordinatlarını (-250, -250) olarak ayarlayın. 
// Grubun merkezi artık (0, 0) x ve y koordinat değerine sahip olacak,
// ve sağ alt köşe (250, 250) konumunda olacaktır.
group.CoordOrigin = new Point(-250, -250);

// Bu grup şeklinin sınırlarını gösterecek bir dikdörtgen oluşturup gruba ekliyoruz.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Bir şekil, bir grup şeklinin parçası olduğunda, ona alt düğüm olarak erişebilir ve onu değiştirebiliriz.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Küçük bir kırmızı yıldız oluşturun ve onu gruba ekleyin.
// Şekli, merkeze taşıdığımız grubun koordinat orijini ile hizalayın.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// Bir dikdörtgen ekleyin ve ardından görselle aynı yere biraz daha küçük bir dikdörtgen ekleyin. 
// Gruba eklediğimiz yeni şekiller eski şekillerle örtüşüyor. Açık mavi dikdörtgen kısmen kırmızı yıldızla örtüşecek,
// ve ardından görüntünün bulunduğu şekil, onu çerçeve olarak kullanarak açık mavi dikdörtgenin üzerine binecek.
// Bir grup şekli içindeki düzenlemelerini değiştirmek için şekillerin "ZOrder" özelliklerini kullanamayız. 
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Grup şekline bir metin kutusu ekleyin. "Sol" özelliğini, metin kutusunun sağ kenarı
// grup şeklinin sağ sınırına dokunur. "Top" özelliğini, metin kutusu dışarıda kalacak şekilde ayarlayın
// üst boyutu grup şeklinin alt kenar boşluğu boyunca sıralanacak şekilde grup şeklinin sınırı.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
