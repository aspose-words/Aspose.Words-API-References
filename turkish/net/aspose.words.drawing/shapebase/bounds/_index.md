---
title: Bounds
second_title: Aspose.Words for .NET API Referansı
description: Şeklin içerdiği bloğun konumunu ve boyutunu alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Şeklin içerdiği bloğun konumunu ve boyutunu alır veya ayarlar.

```csharp
public RectangleF Bounds { get; set; }
```

### Notlar

Ayar yapıldığında en boy oranı kilidini yok sayar.

Üst düzey bir şekil için değer, nokta cinsindendir ve şekil bağlantısına göredir.

Bir gruptaki şekiller için değer, üst grubun koordinat uzayında ve birimlerindedir.

### Örnekler

Blok sınırlarını içeren şeklin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Satırın kendisi belge sayfasında çok az yer kaplasa da,
// boyutunu "Sınırlar" özelliklerini kullanarak belirleyebileceğimiz dikdörtgen içeren bir blok kaplar.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Bir grup şekli oluşturun ve ardından "Sınırlar" özelliğini kullanarak içerdiği bloğun boyutunu ayarlayın.
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

// Grup şeklinin koordinat düzleminin başlangıç noktası, içerdiği bloğun sol üst köşesindedir,
// ve sağ alt köşede (1000, 1000) x ve y koordinatları.
// Grup şeklimiz 250x250pt boyutundadır, yani grup şeklinin koordinat düzlemindeki her 4pt
// belge gövdesinin koordinat düzleminde 1pt'ye çevirir.
// Eklediğimiz her şeklin boyutu da 4 kat küçülecek.
// Şeklin "BoundsInPoints" özelliğindeki değişiklik bunu yansıtacaktır.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Bir şekil ekleyin ve onu grup şeklinin içeren bloğunun sınırlarının dışına yerleştirin.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Grup şeklinin belge gövdesindeki ayak izi arttı, ancak içeren blok aynı kaldı.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

Bir grup şeklinin nasıl oluşturulacağını ve doldurulacağını gösterir.

```csharp
Document doc = new Document();

// Bir grup şekli oluşturun. Bir grup şekli, alt şekil düğümlerinin bir koleksiyonunu görüntüleyebilir.
// Microsoft Word'de grup şeklinin sınırları içine veya grup şeklinin alt şekillerinden birine tıklandığında
// bu gruptaki diğer tüm alt şekilleri seçin ve tüm şekilleri bir kerede ölçeklendirmemize ve taşımamıza izin verin.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// 400pt x 400pt grup şekli oluşturun ve bunu belgenin kayan şekil koordinat orijinine yerleştirin.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Grubun dahili koordinat düzlemi boyutunu 500 x 500pt olarak ayarlayın.
// Grubun sol üst köşesinde bir x ve y koordinatı (0, 0) olacaktır,
// ve sağ alt köşede x ve y koordinatları (500, 500) olacaktır.
group.CoordSize = new Size(500, 500);

 // Grubun sol üst köşesinin koordinatlarını (-250, -250) olarak ayarlayın.
// Grubun merkezi artık bir x ve y koordinat değerine (0, 0) sahip olacak,
// ve sağ alt köşe (250, 250) olacaktır.
group.CoordOrigin = new Point(-250, -250);

// Bu grup şeklinin sınırını gösterecek bir dikdörtgen oluşturun ve onu gruba ekleyin.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Bir şekil bir grup şeklinin parçası olduğunda, ona alt düğüm olarak erişebilir ve sonra değiştirebiliriz.
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

 // Bir dikdörtgen ekleyin ve ardından resimle aynı yere biraz daha küçük bir dikdörtgen ekleyin.
// Gruba eklediğimiz daha yeni şekiller, eski şekillerle örtüşüyor. Açık mavi dikdörtgen, kırmızı yıldızla kısmen örtüşecektir,
// ve ardından görüntülü şekil, onu bir çerçeve olarak kullanarak açık mavi dikdörtgenle örtüşecektir.
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

// Grup şekline bir metin kutusu ekleyin. "Sol" özelliğini, metin kutusunun sağ kenarı olacak şekilde ayarlayın.
// grup şeklinin sağ sınırına dokunur. "Üst" özelliğini, metin kutusu dışarıda kalacak şekilde ayarlayın
// üst boyutu grup şeklinin alt kenar boşluğu boyunca sıralanmış olarak grup şeklinin sınırı.
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
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
