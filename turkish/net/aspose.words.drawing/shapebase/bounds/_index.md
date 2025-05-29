---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: .NET için Aspose.Words
description: Şeklinizin konumunu ve boyutunu zahmetsizce yönetmek, tasarım hassasiyetinizi ve verimliliğinizi artırmak için ShapeBase Bounds özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Şeklin içeren bloğunun konumunu ve boyutunu alır veya ayarlar.

```csharp
public RectangleF Bounds { get; set; }
```

## Notlar

Ayarlandığında en boy oranı kilidini yok sayar.

En üst düzey bir şekil için değer, nokta cinsindendir ve şekil çapa noktasına göredir.

Bir gruptaki şekiller için değer, üst grubun koordinat alanında ve birimlerindedir.

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
