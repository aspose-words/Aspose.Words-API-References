---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Shape sınıf. Otomatik Şekil metin kutusu serbest biçim OLE nesnesi ActiveX denetimi veya resim gibi çizim katmanındaki bir nesneyi temsil eder C#'da.
type: docs
weight: 1250
url: /tr/net/aspose.words.drawing/shape/
---
## Shape class

Otomatik Şekil, metin kutusu, serbest biçim, OLE nesnesi, ActiveX denetimi veya resim gibi çizim katmanındaki bir nesneyi temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Şekillerle Çalışmak](https://docs.aspose.com/words/net/working-with-shapes/) dokümantasyon makalesi.

```csharp
public sealed class Shape : ShapeBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | Yeni bir şekil nesnesi oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Bu şeklin diğer şekillerle örtüşüp çakışmayacağını belirten bir değer alır veya ayarlar. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Grafik yerine görüntülenecek alternatif metni tanımlar. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Şeklin bağlantısının kilitli olup olmadığını belirtir. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Şeklin en boy oranının kilitli olup olmadığını belirtir. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Şeklin metnin altında mı yoksa üstünde mi olacağını belirtir. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Şeklin taşıyıcı bloğunun alt kenarının konumunu alır. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Şeklin bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | En üstteki şeklin bağlantısına göre, şeklin içerdiği blokun konumunu ve boyutunu noktalar cinsinden alır. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son boyutu alır. Değer, nokta cinsinden ölçülür. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | İadeler`doğru` şekil türü, şeklin bir resme sahip olmasına izin veriyorsa. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Bu şeklin bir özelliği varsa grafik özelliklerine erişim sağlar[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Bu şeklin bulunduğu bloğun sol üst köşesindeki koordinatlar. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Bu şeklin bulunduğu bloğun içindeki koordinat alanının genişliği ve yüksekliği. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Belge metni ile şeklin alt kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Belge metni ile şeklin sol kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Belge metni ile şeklin sağ kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | İadeler`doğru` ekstrüzyon efekti etkinse. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Şeklin dolgu formatını alır. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Şeklin kapalı yolunu dolduran fırça rengini tanımlar. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Şeklin kapalı yolunun doldurulup doldurulmayacağını belirler. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Şeklin ilk paragrafını alır. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Şeklin yönünü değiştirir. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Bu nesnenin yazı tipi formatlamasına erişim sağlar. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | İadeler`doğru` Eğer bu`Shape` bir var[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | İadeler`doğru` bu düğümün herhangi bir alt düğümü varsa. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | İadeler`doğru` şeklin görüntü baytları varsa veya bir görüntüye bağlantı veriyorsa. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | İadeler`doğru` Eğer bu`Shape` bir SmartArt nesnesi var. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Şeklin bulunduğu bloğun yüksekliğini alır veya ayarlar. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Şeklin göreceli yüksekliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Şeklin yatay olarak nasıl konumlandırılacağını belirtir. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Yatay kural şeklinin özelliklerine erişim sağlar. Yatay kural olmayan bir şekil için şunu döndürür:`hükümsüz` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Bir şeklin tam köprü adresini alır veya ayarlar. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Şeklin görüntüsüne erişim sağlar. Döndürür`hükümsüz` şeklin bir resmi olamazsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | İadeler`doğru` çünkü bu düğüm alt düğümlere sahip olabilir. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Belgedeki şeklin dekoratif olup olmadığını belirten bayrağı alır veya ayarlar. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | İadeler`doğru` eğer bu bir grup şekli ise. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | İadeler`doğru` eğer bu şekil yatay bir kural ise. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | İadeler`doğru` bu şekil bir resim şekli ise. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Bu şeklin metinle satır içi olarak konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Şeklin tablonun içinde mi yoksa dışında mı görüntüleneceğini belirten bir bayrak alır veya ayarlar. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Şeklin bir olduğunu belirtir[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | İadeler`doğru`bu şekil bir grup şeklinin alt öğesi değilse. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | İadeler`doğru` bu şekil bir WordArt nesnesiyse. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Şeklin son paragrafını alır. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Şeklin içeren bloğunun sol kenarının konumunu alır veya ayarlar. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Şeklin göreceli sol konumunu yüzde cinsinden temsil eden değeri alır veya ayarlar. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Bu grafik nesnesi için kullanılan MarkupLanguage'ı döndürür. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | İsteğe bağlı şekil adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | İadelerShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Bir şeklin OLE verilerine erişim sağlar. OLE nesnesi veya ActiveX denetimi olmayan bir şekil için şunu döndürür:`hükümsüz` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Doğrudan üst paragrafı döndürür. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../../aspose.words/range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Şeklin yatay olarak nasıl konumlandırılacağına göre belirtir. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Şeklin göreceli boyutunun değerini yatay yönde alır veya ayarlar. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Şeklin dikey olarak neye göre konumlandırıldığını belirtir. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Şeklin göreli boyutunun değerini dikey yönde alır veya ayarlar. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Şeklin içeren bloğunun sağ kenarının konumunu alır. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Şeklin döndürüldüğü açıyı (derece cinsinden) tanımlar. Pozitif değer, saat yönünde dönüş açısına karşılık gelir. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Fare işaretçisi şeklin üzerine geldiğinde görüntülenecek metni tanımlar. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | İadeler`doğru` gölge efekti etkinse. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Şeklin gölge formatını alır. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Şekil türünü alır. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Alır[`SignatureLine`](../signatureline/) Şekil bir imza çizgisiyse nesne. İadeler`hükümsüz` aksi halde. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Şeklin boyutunu nokta cinsinden alır. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | İadelerTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Bir şeklin konturunu tanımlar. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Konturun rengini tanımlar. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Yolun vuruşlu olup olmayacağını tanımlar. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Bir şeklin yolunu nokta olarak konturlayan fırça kalınlığını tanımlar. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Şekil köprüsü için hedef çerçeveyi alır veya ayarlar. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Metnin bir şekilde nasıl görüntüleneceğini belirten nitelikleri tanımlar. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Metin yolunun metnini (bir WordArt nesnesinin) tanımlar. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Geçerli şekil nesnesinin başlığını (başlığını) alır veya ayarlar. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Şeklin içeren bloğunun üst kenarının konumunu alır veya ayarlar. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Şeklin göreli üst konumunu yüzde cinsinden temsil eden değeri alır veya ayarlar. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Şeklin dikey olarak nasıl konumlandırılacağını belirtir. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Şeklin içeren bloğunun genişliğini alır veya ayarlar. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Şeklin göreceli genişliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Metnin şeklin etrafına nasıl sarıldığını belirtir. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Şeklin satır içi mi yoksa kayan mı olduğunu tanımlar. Kayan şekiller için, şeklin etrafındaki metin için kaydırma modunu tanımlar. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Çakışan şekillerin görüntülenme sırasını belirler. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Ziyaretçi kabul eder. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Efekt kapsamının kaynak dikdörtgen değerlerine eklenir ve son dikdörtgeni döndürür. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Bu şekli bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Belirtilen düğümü, belirtilen referans düğümünün hemen sonrasına ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Belirtilen düğümü, belirtilen referans düğümünün hemen öncesine ekler. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Yerel koordinat alanından bir değeri üst şeklin koordinat alanına dönüştürür. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Belirtilen alt düğümü kaldırır. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/)Geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Sistem kullanımı için ayrılmıştır. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Aspose.Words'ün SmartArt soğuk işleme motorunu kullanarak SmartArt önceden oluşturulmuş çizimi günceller. |

## Notlar

Kullanmak`Shape` sınıfında bir Microsoft Word belgesinde şekiller oluşturabilir veya değiştirebilirsiniz.

Bir şeklin önemli bir özelliği onun[`ShapeType`](../shapebase/shapetype/)Farklı türlerindeki şekiller, bir Word belgesinde farklı yeteneklere sahip olabilir. Örneğin, yalnızca görüntünün ve OLE şekil 'nin içlerinde görüntüler bulunabilir. Şekillerin çoğunda metin bulunabilir, ancak hepsinde olmayabilir.

Metin içerebilen şekiller şunları içerebilir[`Paragraph`](../../aspose.words/paragraph/) ve [`Table`](../../aspose.words.tables/table/) çocuklar gibi düğümler.

## Örnekler

Sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Çakışan metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
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

// Belgedeki şekillerin koleksiyonunu alın,
// ve resim içeren her şeklin resim verilerini dosya olarak yerel dosya sistemine kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Şekillerin görüntü verileri birçok olası görüntü formatındaki görüntüleri içerebilir.
        // Her görsel için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bir belgedeki tüm şekillerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İki şekli, içinde başka bir şekil bulunan bir grup şekliyle birlikte ekleyin.
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

// Tüm Şekil düğümlerini belgeden kaldırın.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Tüm şekiller gitti ancak grup şekli hâlâ belgede.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Tüm grup şekillerini ayrı ayrı kaldırın.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* class [ShapeBase](../shapebase/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
