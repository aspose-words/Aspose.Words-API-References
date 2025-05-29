---
title: ShapeBase.CoordSize
linktitle: CoordSize
articleTitle: CoordSize
second_title: .NET için Aspose.Words
description: Tasarım projelerinizde optimum düzen kontrolü için koordinat alanının genişliğini ve yüksekliğini tanımlayan ShapeBase CoordSize özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

Bu şeklin bulunduğu bloğun içindeki koordinat alanının genişliği ve yüksekliği.

```csharp
public Size CoordSize { get; set; }
```

## Notlar

Varsayılan değer (1000, 1000)'dir.

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

Bir grup şeklinin nasıl oluşturulacağını ve doldurulacağını gösterir.

```csharp
Document doc = new Document();

// Bir grup şekli oluşturun. Bir grup şekli, bir dizi alt şekil düğümünü görüntüleyebilir.
// Microsoft Word'de, grup şeklinin sınırları içinde veya grup şeklinin alt şekillerinden birinin üzerine tıklamak,
// Bu gruptaki diğer tüm alt şekilleri seç ve tüm şekilleri aynı anda ölçeklememize ve taşımamıza izin ver.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// 400pt x 400pt boyutlarında bir grup şekli oluşturun ve bunu belgenin kayan şeklinin koordinat kökenine yerleştirin.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Grubun iç koordinat düzlemi boyutunu 500 x 500pt olarak ayarlayın.
// Grubun sol üst köşesi (0, 0) x ve y koordinatına sahip olacak,
// ve sağ alt köşede x ve y koordinatları (500, 500) olacaktır.
group.CoordSize = new Size(500, 500);

 // Grubun sol üst köşesinin koordinatlarını (-250, -250) olarak ayarla.
// Grubun merkezi artık (0, 0) x ve y koordinat değerine sahip olacak,
// ve sağ alt köşe (250, 250) noktasında olacak.
group.CoordOrigin = new Point(-250, -250);

// Bu grup şeklinin sınırını görüntüleyecek bir dikdörtgen oluştur ve bunu gruba ekle.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// Bir şekil bir grup şeklinin parçası olduğunda, ona bir alt düğüm olarak erişebilir ve ardından onu değiştirebiliriz.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Küçük kırmızı bir yıldız oluşturup gruba ekleyin.
// Şekli, merkeze taşıdığımız grubun koordinat orijinine hizalayalım.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Bir dikdörtgen ekleyin ve ardından aynı yere bir resimle birlikte biraz daha küçük bir dikdörtgen ekleyin.
// Gruba eklediğimiz yeni şekiller eski şekillerin üzerine biner. Açık mavi dikdörtgen kırmızı yıldızın üzerine kısmen biner.
// ve daha sonra resimli şekil, açık mavi dikdörtgenin üzerine gelecek ve onu çerçeve olarak kullanacaktır.
// Şekillerin bir grup şekli içindeki düzenlemelerini değiştirmek için "ZOrder" özelliklerini kullanamayız.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Grup şekline bir metin kutusu ekleyin. "Sol" özelliğini, metin kutusunun sağ kenarının
// grup şeklinin sağ sınırına dokunur. "Üst" özelliğini, metin kutusunun dışarıda yer alması için ayarlayın
// grup şeklinin sınırı, üst boyutu grup şeklinin alt kenarı boyunca hizalanmış şekilde.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

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
