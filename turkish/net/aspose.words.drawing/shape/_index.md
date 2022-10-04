---
title: Shape
second_title: Aspose.Words for .NET API Referansı
description: Otomatik Şekil metin kutusu serbest biçim OLE nesnesi ActiveX denetimi veya resim gibi çizim katmanındaki bir nesneyi temsil eder.
type: docs
weight: 1100
url: /tr/net/aspose.words.drawing/shape/
---
## Shape class

Otomatik Şekil, metin kutusu, serbest biçim, OLE nesnesi, ActiveX denetimi veya resim gibi çizim katmanındaki bir nesneyi temsil eder.

```csharp
public sealed class Shape : ShapeBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Shape](shape/)(DocumentBase, ShapeType) | Yeni bir şekil nesnesi oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Bu şeklin diğer şekillerle örtüşüp örtüşmeyeceğini belirten bir değer alır veya ayarlar. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Grafik yerine görüntülenecek alternatif metni tanımlar. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Şeklin bağlantısının kilitli olup olmadığını belirtir. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Şeklin en boy oranının kilitli olup olmadığını belirtir. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Şeklin içeren bloğunun alt kenarının konumunu alır. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Şeklin içerdiği bloğun konumunu ve boyutunu alır veya ayarlar. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | En üstteki şeklin bağlantısına göre, şekli içeren bloğun konumunu ve boyutunu nokta olarak alır. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son kapsamı alır. Değer, noktalarla ölçülür. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Şekil türü, şeklin bir görüntüye sahip olmasına izin veriyorsa true değerini döndürür. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Bu şeklin bir Grafiği varsa, grafik özelliklerine erişim sağlar. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Bu şekli içeren bloğun sol üst köşesindeki koordinatlar. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Bu şeklin içerdiği bloğun içindeki koordinat uzayının genişliği ve yüksekliği. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Belge metni ile şeklin alt kenarı arasındaki mesafeyi (nokta olarak) döndürür veya ayarlar. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Belge metni ile şeklin sol kenarı arasındaki mesafeyi (nokta olarak) döndürür veya ayarlar. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Belge metni ile şeklin sağ kenarı arasındaki mesafeyi (nokta olarak) döndürür veya ayarlar. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta olarak) döndürür veya ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Bir ekstrüzyon efekti etkinleştirilirse true değerini döndürür. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Şekil için dolgu biçimlendirmesini alır. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Şeklin kapalı yolunu dolduran fırça rengini tanımlar. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Şeklin kapalı yolunun doldurulup doldurulmayacağını belirler. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Şekildeki ilk paragrafı alır. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Şeklin yönünü değiştirir. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Bu Şeklin bir[`Chart`](./chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Şekilde görüntü baytları varsa veya bir görüntüye bağlanırsa true değerini döndürür. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Bu Shape bir SmartArt nesnesine sahipse true döndürür. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Şeklin içerdiği bloğun yüksekliğini alır veya ayarlar. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Şeklin yatay olarak nasıl konumlandırılacağını belirtir. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Yatay kural şeklinin özelliklerine erişim sağlar. Yatay kural olmayan bir şekil için null döndürür. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Bir şekil için tam köprü adresini alır veya ayarlar. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Şeklin görüntüsüne erişim sağlar. Şeklin görüntüsü yoksa null değerini döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Şeklin belgede dekoratif olup olmadığını belirten bayrağı alır veya ayarlar. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Bu bir grup şekliyse true değerini döndürür. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Bu şekil yatay bir kural ise true değerini döndürür. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Bu şekil bir görüntü şekliyse true değerini döndürür. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Bu şeklin metinle aynı hizada olup olmadığını belirlemenin hızlı bir yolu. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Şeklin bir tablonun içinde mi yoksa dışında mı görüntülendiğini belirten bir bayrak alır veya ayarlar. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Şeklin bir SignatureLine olduğunu gösterir. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Bu şekil bir grup şeklinin alt öğesi değilse true değerini döndürür. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Bu şekil bir WordArt nesnesiyse true değerini döndürür. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Şekildeki son paragrafı alır. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Şeklin içeren bloğunun sol kenarının konumunu alır veya ayarlar. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Bu grafik nesnesi için kullanılan İşaretleme Dilini alır. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | İsteğe bağlı şekil adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | İadeShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Bir şeklin OLE verilerine erişim sağlar. OLE nesnesi veya ActiveX denetimi olmayan bir şekil için null. döndürür |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Hemen üst paragrafı döndürür. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Şeklin yatay olarak neye göre konumlandırıldığını belirtir. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Şeklin dikey olarak neye göre konumlandırıldığını belirtir. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Şeklin içeren bloğunun sağ kenarının konumunu alır. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Şeklin döndürüldüğü açıyı (derece olarak) tanımlar. Pozitif değer, saat yönünde dönüş açısına karşılık gelir. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Fare işaretçisi şeklin üzerine geldiğinde görüntülenen metni tanımlar. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Bir gölge efekti etkinleştirilirse true değerini döndürür. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Şekil için gölge biçimlendirmesini alır. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Şekil türünü alır. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Alır[`SignatureLine`](./signatureline/) şekil bir imza satırı ise nesne. İadeler **hükümsüz** aksi halde. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Şeklin boyutunu nokta olarak alır. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | İadeTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Bir şekil için kontur tanımlar. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Konturun rengini tanımlar. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Yolun konturlu olup olmayacağını tanımlar. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Bir şeklin yolunu nokta olarak çizen fırça kalınlığını tanımlar. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Şekil köprüsü için hedef çerçeveyi alır veya ayarlar. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Metnin bir şekilde nasıl görüntüleneceğini belirleyen özellikleri tanımlar. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Metin yolunun (bir WordArt nesnesinin) metnini tanımlar. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Geçerli şekil nesnesinin başlığını (başlık) alır veya ayarlar. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Şeklin içeren bloğunun üst kenarının konumunu alır veya ayarlar. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Şeklin dikey olarak nasıl konumlandırılacağını belirtir. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Şeklin içerdiği bloğun genişliğini alır veya ayarlar. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Metnin şeklin etrafına nasıl sarılacağını belirtir. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Şeklin satır içi mi yoksa kayan mı olduğunu tanımlar. Kayan şekiller için, şeklin etrafındaki metin için kaydırma modunu tanımlar. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Çakışan şekillerin görüntülenme sırasını belirler. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | Efekt kapsamının kaynak dikdörtgen değerlerini ekler ve son dikdörtgeni döndürür. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Bu şekli bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | Yerel koordinat alanından bir değeri ana şeklin koordinat alanına dönüştürür. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Aspose.Words'ün SmartArt soğuk işleme motorunu kullanarak SmartArt önceden oluşturulmuş çizimi günceller. |

### Notlar

Kullanmak[`Shape`](./shape/) bir Microsoft Word belgesinde şekiller oluşturabilir veya değiştirebilirsiniz.

Bir şeklin önemli bir özelliği, onun[`ShapeType`](../shapebase/shapetype/). Farklı türlerindeki şekiller, bir Word belgesinde farklı yeteneklere sahip olabilir. Örneğin, yalnızca resim ve OLE shape içinde resimler olabilir. Şekillerin çoğunda metin olabilir, ancak hepsinde olmayabilir.

Metin içerebilen, içerebilen şekiller[`Paragraph`](../../aspose.words/paragraph/) and [`Table`](../../aspose.words.tables/table/) çocuklar gibi düğümler.

### Örnekler

Bir sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste binen metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgeden şekil koleksiyonunu alın,
// ve bir görüntü ile her şeklin görüntü verilerini yerel dosya sistemine dosya olarak kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Şekillerin görüntü verileri, birçok olası görüntü formatının görüntülerini içerebilir. 
        // Her resim için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bir belgeden tüm şekillerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçinde başka bir şekil olan bir grup şekliyle birlikte iki şekil ekleyin.
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// Belgeden tüm Shape düğümlerini kaldırın.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Tüm şekiller gitti, ancak grup şekli hala belgede.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Tüm grup şekillerini ayrı ayrı kaldır.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* class [ShapeBase](../shapebase/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
