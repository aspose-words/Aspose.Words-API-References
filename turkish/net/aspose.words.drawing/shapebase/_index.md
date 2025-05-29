---
title: ShapeBase Class
linktitle: ShapeBase
articleTitle: ShapeBase
second_title: .NET için Aspose.Words
description: AutoShapes, OLE nesneleri ve ActiveX denetimleri de dahil olmak üzere dinamik çizimler oluşturmak için temeliniz olan Aspose.Words.Drawing.ShapeBase sınıfını keşfedin.
type: docs
weight: 1650
url: /tr/net/aspose.words.drawing/shapebase/
---
## ShapeBase class

Çizim katmanındaki nesneler için temel sınıf, örneğin Otomatik Şekil, serbest biçim, OLE nesnesi, ActiveX denetimi veya resim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Şekillerle Çalışma](https://docs.aspose.com/words/net/working-with-shapes/) belgeleme makalesi.

```csharp
public abstract class ShapeBase : CompositeNode
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Bu şeklin diğer şekillerle örtüşüp örtüşmeyeceğini belirten bir değer alır veya ayarlar. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Grafik yerine görüntülenecek alternatif metni tanımlar. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Şeklin bağlantısının kilitli olup olmadığını belirtir. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Şeklin en boy oranının kilitli olup olmadığını belirtir. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Şeklin içeren bloğunun alt kenarının konumunu alır. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Şeklin içeren bloğunun konumunu ve boyutunu alır veya ayarlar. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Şeklin içeren bloğunun konumunu ve boyutunu, en üstteki şeklin çapa noktasına göre noktalar halinde alır. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son kapsamı alır. Değer noktalarla ölçülür. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Geri Döndürür`doğru` eğer şekil türü şeklin bir görüntüye sahip olmasına izin veriyorsa. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Bu şeklin bulunduğu bloğun sol üst köşesindeki koordinatlar. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Bu şeklin bulunduğu bloğun içindeki koordinat alanının genişliği ve yüksekliği. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Belge metni ile şeklin alt kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Belge metni ile şeklin sol kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Belge metni ile şeklin sağ kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Şekil için dolgu biçimlendirmesini alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Bir şeklin yönünü değiştirir. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Şekil için parıltı biçimlendirmesini alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Şeklin içeren bloğunun yüksekliğini alır veya ayarlar. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Şeklin göreli yüksekliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Şeklin görünür olup olmadığını belirten bir Boole değeri alır veya ayarlar. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Şeklin yatay olarak nasıl konumlandırılacağını belirtir. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Bir şeklin tam köprü adresini alır veya ayarlar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Şeklin belgede dekoratif olup olmadığını belirten bayrağı alır veya ayarlar. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Geri Döndürür`doğru` eğer bu bir grup şekliyse. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Geri Döndürür`doğru` eğer bu şekil yatay bir cetvel ise. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Geri Döndürür`doğru` eğer bu şekil bir görüntü şekliyse. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Bu şeklin metinle aynı hizada konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Şeklin bir tablonun içinde mi yoksa dışında mı görüntüleneceğini belirten bir bayrak alır veya ayarlar. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Şeklin bir[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Geri Döndürür`doğru` eğer bu şekil bir grup şeklinin çocuğu değilse. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Geri Döndürür`doğru` eğer bu şekil bir WordArt nesnesiyse. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Şeklin içeren bloğunun sol kenarının konumunu alır veya ayarlar. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Şeklin yüzde olarak göreli sol konumunu temsil eden değeri alır veya ayarlar. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Bu grafik nesnesi için kullanılan MarkupLanguage'ı alır. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | İsteğe bağlı şekil adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Hemen üst paragrafı döndürür. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Şekil için yansıma biçimlendirmesini alır. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Şeklin yatay olarak nasıl konumlandırıldığını belirtir. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Şeklin yatay yöndeki göreli boyutunun değerini alır veya ayarlar. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Şeklin dikey olarak nasıl konumlandırıldığını belirtir. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Şeklin dikey yöndeki göreli boyutunun değerini alır veya ayarlar. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Şeklin içeren bloğunun sağ kenarının konumunu alır. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Bir şeklin döndürüleceği açıyı (derece olarak) tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Fare işaretçisi şeklin üzerine geldiğinde görüntülenen metni tanımlar. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Şekil için gölge biçimlendirmesi alır. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Şekil türünü alır. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Şeklin boyutunu noktalar halinde alır. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Şekil için yumuşak kenar biçimlendirmesi alır. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Şekil köprüsü için hedef çerçeveyi alır veya ayarlar. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Geçerli şekil nesnesinin başlığını (başlığını) alır veya ayarlar. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Şeklin içeren bloğunun üst kenarının konumunu alır veya ayarlar. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Şeklin yüzde olarak göreli en üst konumunu temsil eden değeri alır veya ayarlar. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Şeklin dikey olarak nasıl konumlandırılacağını belirtir. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Şeklin içeren bloğunun genişliğini alır veya ayarlar. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Şeklin göreli genişliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Metnin şeklin etrafına nasıl sarılacağını belirtir. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Şeklin satır içi mi yoksa yüzen mi olduğunu tanımlar. Yüzen şekiller için şeklin etrafındaki metnin sarma modunu tanımlar. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Çakışan şekillerin görüntülenme sırasını belirler. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd yöntemini çağırır. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart yöntemini çağırır. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Kaynak dikdörtgene efekt kapsamının değerlerini ekler ve son dikdörtgeni döndürür. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Bu şekli bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Yerel koordinat alanındaki bir değeri ana şeklin koordinat alanına dönüştürür. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Bu soyut bir sınıftır. instantiate yapabileceğiniz iki türetilmiş sınıf şunlardır:[`Shape`](../shape/) Ve[`GroupShape`](../groupshape/).

Şekil, belge ağacındaki bir düğümdür.

Şekil bir çocuğun şekli ise[`Paragraph`](../../aspose.words/paragraph/) nesne ise, o zaman şeklin "en üst düzey" olduğu söylenir. En üst düzey şekiller noktalar halinde ölçülür ve konumlandırılır.

Bir şekil aynı zamanda bir çocuğun çocuğu olarak da ortaya çıkabilir[`GroupShape`](../groupshape/) Birkaç şekil gruplandığında nesne. Bir grup şeklinin alt şekilleri koordinat alanına yerleştirilir ve birimler tarafından tanımlanır[`CoordSize`](./coordsize/) Ve[`CoordOrigin`](./coordorigin/) parent grup şeklinin özellikleri.

Bir şekil metinle satır içi veya yüzer şekilde konumlandırılabilir. Konumlandırma yöntemi, şu şekilde kontrol edilir:[`WrapType`](./wraptype/) mülk.

Bir şekil yüzdüğünde, bir şeye göre konumlandırılır (örneğin geçerli paragraf, kenar boşluğu veya sayfa). Şeklin göreceli konumlandırılması, kullanılarak belirtilir.[`RelativeHorizontalPosition`](./relativehorizontalposition/) Ve[`RelativeVerticalPosition`](./relativeverticalposition/) özellikler.

Yüzen bir şekil, açıkça kullanılarak konumlandırılabilir[`Left`](./left/) Ve[`Top`](./top/) özellikleri veya başka bir nesneye göre hizalanmış[`HorizontalAlignment`](./horizontalalignment/) ve[`VerticalAlignment`](./verticalalignment/) özellikler.

## Örnekler

Sayfanın ortasına kayan bir resmin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste gelen metnin arkasında görünecek yüzen bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
