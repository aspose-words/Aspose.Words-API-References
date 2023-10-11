---
title: ShapeBase.Bounds
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Şeklin bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar.

```csharp
public RectangleF Bounds { get; set; }
```

### Notlar

Ayarlama sonrasında en boy oranı kilidini yok sayar.

Üst düzey bir şekil için değer nokta cinsindendir ve şekil bağlantısına göredir.

Bir gruptaki şekiller için değer, üst grubun koordinat alanında ve birimlerindedir.

### Örnekler

Blok sınırlarını içeren şeklin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Satırın kendisi belge sayfasında çok az yer kaplasa da,
// "Sınır" özelliklerini kullanarak boyutunu belirleyebileceğimiz dikdörtgen içeren bir bloğu kaplar.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Bir grup şekli oluşturun ve ardından "Sınır" özelliğini kullanarak onu içeren bloğun boyutunu ayarlayın.
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

// Grup şeklinin koordinat düzleminin başlangıç noktası, bulunduğu bloğun sol üst köşesindedir,
// ve sağ alt köşedeki (1000, 1000)'in x ve y koordinatları.
// Grup şeklimiz 250x250pt boyutunda, yani grup şeklinin koordinat düzlemindeki her 4pt
// belge gövdesinin koordinat düzleminde 1pt'ye çevrilir.
// Eklediğimiz her şeklin boyutu da 4 kat küçülecektir.
// Şeklin "BoundsInPoints" özelliğindeki değişiklik bunu yansıtacaktır.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Bir şekil ekleyin ve onu, grup şeklinin bulunduğu bloğun sınırlarının dışına yerleştirin.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// Grup şeklinin belge gövdesindeki kapladığı alan arttı ancak içeren blok aynı kaldı.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


