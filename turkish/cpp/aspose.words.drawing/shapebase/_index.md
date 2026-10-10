---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase class. Çizim katmanındaki nesneler için temel sınıf, örneğin AutoShape, serbest şekil, OLE nesnesi, ActiveX denetimi veya resim. Daha fazla bilgi edinmek için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


AutoShape, serbest şekil, OLE nesnesi, ActiveX denetimi veya resim gibi çizim katmanındaki nesneler için temel sınıftır. Daha fazla bilgi edinmek için [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) dokümantasyon makalesini ziyaret edin.

```cpp
class ShapeBase : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IInline,
                  public Aspose::Words::Drawing::Core::IShape,
                  public Aspose::Words::IShapeAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode,
                  public Aspose::Words::Drawing::Core::IFillable,
                  public Aspose::Words::Drawing::Core::IGlow,
                  public Aspose::Words::Drawing::Core::IReflection,
                  public Aspose::Words::Drawing::Core::ISoftEdge,
                  public Aspose::Words::Drawing::Core::IShadow
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Bir ziyaretçiyi kabul eder. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXEnd metodunu çağırır. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Türetilmiş bir sınıfta uygulandığında, belirtilen belge ziyaretçisinin VisitXXXStart metodunu çağırır. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Kaynak dikdörtgene etki genişliğinin değerlerini ekler ve son dikdörtgeni döndürür. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_AllowOverlap](./get_allowoverlap/)() | Bu şeklin diğer şekillerin üzerine çıkıp çıkamayacağını belirten bir değeri alır veya ayarlar. |
| [get_AlternativeText](./get_alternativetext/)() | Grafik yerine gösterilecek alternatif metni tanımlar. |
| [get_AnchorLocked](./get_anchorlocked/)() | Şeklin çapa noktasının kilitli olup olmadığını belirtir. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Şeklin en‑boy oranının kilitli olup olmadığını belirtir. |
| [get_BehindText](./get_behindtext/)() | Şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir. |
| [get_Bottom](./get_bottom/)() | Şeklin içinde bulunduğu bloğun alt kenar konumunu alır. |
| [get_Bounds](./get_bounds/)() | Şeklin içinde bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | En üst şeklin çapa noktasına göre, şeklin içinde bulunduğu bloğun konumunu ve boyutunu nokta cinsinden alır. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son kapsamı alır. Değer nokta cinsinden ölçülür. |
| [get_CanHaveImage](./get_canhaveimage/)() | Şekil türü şeklin bir görüntüye sahip olmasına izin veriyorsa **true** döndürür. |
| [get_CoordOrigin](./get_coordorigin/)() | Bu şeklin içinde bulunduğu bloğun sol üst köşesindeki koordinatlar. |
| [get_CoordSize](./get_coordsize/)() | Bu şeklin içinde bulunduğu bloğun içindeki koordinat alanının genişliği ve yüksekliği. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_DistanceBottom](./get_distancebottom/)() | Belge metni ile şeklin alt kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| [get_DistanceLeft](./get_distanceleft/)() | Belge metni ile şeklin sol kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| [get_DistanceRight](./get_distanceright/)() | Belge metni ile şeklin sağ kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| [get_DistanceTop](./get_distancetop/)() | Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_Fill](./get_fill/)() | Şekil için dolgu biçimlendirmesini alır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FlipOrientation](./get_fliporientation/)() | Bir şeklin yönünü değiştirir. |
| [get_Font](./get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Glow](./get_glow/)() | Şekil için parıltı biçimlendirmesini alır. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_Height](./get_height/)() | Şeklin içinde bulunduğu bloğun yüksekliğini alır veya ayarlar. |
| [get_HeightRelative](./get_heightrelative/)() | Şeklin göreceli yüksekliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [get_Hidden](./get_hidden/)() | Şeklin görünür olup olmadığını gösteren bir boolean değeri alır veya ayarlar. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Şeklin yatay olarak nasıl konumlandırıldığını belirtir. |
| [get_HRef](./get_href/)() | Bir şekil için tam hiperlink adresini alır veya ayarlar. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsDecorative](./get_isdecorative/)() | Şeklin belgede dekoratif olup olmadığını belirten bayrağı alır veya ayarlar. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsGroup](./get_isgroup/)() | Bu bir grup şekil ise **true** döndürür. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Bu şekil bir yatay kural ise **true** döndürür. |
| [get_IsImage](./get_isimage/)() | Bu şekil bir resim şekli ise **true** döndürür. |
| [get_IsInline](./get_isinline/)() | Bu şeklin metin içinde satır içi konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Şeklin bir tablo içinde mi yoksa dışında mı görüntülendiğini gösteren bayrağı alır veya ayarlar. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_IsSignatureLine](./get_issignatureline/)() | Şeklin bir [SignatureLine](../signatureline/) olduğunu gösterir. |
| [get_IsTopLevel](./get_istoplevel/)() | Bu şekil bir grup şeklin çocuğu değilse **true** döndürür. |
| [get_IsWordArt](./get_iswordart/)() | Bu şekil bir WordArt nesnesi ise **true** döndürür. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_Left](./get_left/)() | Şeklin içinde bulunduğu bloğun sol kenar konumunu alır veya ayarlar. |
| [get_LeftRelative](./get_leftrelative/)() | Şeklin yüzde olarak göreceli sol konumunu temsil eden değeri alır veya ayarlar. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Bu grafik nesnesi için kullanılan MarkupLanguage'ı alır. |
| [get_Name](./get_name/)() | İsteğe bağlı şekil adını alır veya ayarlar. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Bu düğümün tipini alır. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](./get_parentparagraph/)() | Doğrudan üst paragrafı döndürür. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_Reflection](./get_reflection/)() | Şekil için yansıma biçimlendirmesini alır. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Şeklin yatay olarak neye göre konumlandırıldığını belirtir. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Şeklin yatay yönde göreceli boyut değerini alır veya ayarlar. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Şeklin dikey olarak neye göre konumlandırıldığını belirtir. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Şeklin dikey yönde göreceli boyut değerini alır veya ayarlar. |
| [get_Right](./get_right/)() | Şeklin içinde bulunduğu bloğun sağ kenar konumunu alır. |
| [get_Rotation](./get_rotation/)() | Bir şeklin döndürüldüğü açıyı (derece cinsinden) tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir. |
| [get_ScreenTip](./get_screentip/)() | Fare işaretçisi şeklin üzerine hareket ettiğinde gösterilen metni tanımlar. |
| [get_ShadowFormat](./get_shadowformat/)() | Şekil için gölge biçimlendirmesini alır. |
| [get_ShapeType](./get_shapetype/)() | Şekil tipini alır. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Şeklin boyutunu puan cinsinden alır. |
| [get_SoftEdge](./get_softedge/)() | Şekil için yumuşak kenar biçimlendirmesini alır. |
| [get_Target](./get_target/)() | Şekil bağlantısı için hedef çerçeveyi alır veya ayarlar. |
| [get_Title](./get_title/)() | Mevcut şekil nesnesinin başlığını (alt yazısını) alır veya ayarlar. |
| [get_Top](./get_top/)() | Şeklin içinde bulunduğu bloğun üst kenar konumunu alır veya ayarlar. |
| [get_TopRelative](./get_toprelative/)() | Şeklin yüzde cinsinden göreceli üst konumunu temsil eden değeri alır veya ayarlar. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Şeklin dikey olarak nasıl konumlandırıldığını belirtir. |
| [get_Width](./get_width/)() | Şeklin içinde bulunduğu bloğun genişliğini alır veya ayarlar. |
| [get_WidthRelative](./get_widthrelative/)() | Şeklin göreceli genişliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [get_WrapSide](./get_wrapside/)() | Metnin şeklin etrafında nasıl kaydırıldığını belirtir. |
| [get_WrapType](./get_wraptype/)() | Şeklin satır içinde mi yoksa yüzen mi olduğunu tanımlar. Yüzen şekiller için metnin şeklin etrafındaki kaydırma modunu tanımlar. |
| [get_ZOrder](./get_zorder/)() | Üst üste binen şekillerin görüntüleme sırasını belirler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetShapeRenderer](./getshaperenderer/)() | Bu şekli bir görüntüye renderlemek için kullanılabilecek bir nesne oluşturur ve döndürür. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Bir değeri yerel koordinat alanından üst şeklin koordinat alanına dönüştürür. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../../aspose.words/node/) öğesini seçer. |
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_DistanceBottom](./set_distancebottom/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu bir soyut sınıftır. Oluşturabileceğiniz iki türetilmiş sınıf [Shape](../shape/) ve [GroupShape](../groupshape/).

Bir şekil, belge ağacındaki bir düğümdür.

Eğer şekil bir [Paragraph](../../aspose.words/paragraph/) nesnesinin çocuğuysa, şekil "üst düzey" olarak adlandırılır. Üst düzey şekiller puan cinsinden ölçülür ve konumlandırılır.

Bir şekil, birkaç şekil gruplanmış olduğunda bir [GroupShape](../groupshape/) nesnesinin çocuğu olarak da bulunabilir. Bir grup şeklinin çocuk şekilleri, ebeveyn grup şeklinin [CoordSize](./get_coordsize/) ve [CoordOrigin](./get_coordorigin/) özellikleriyle tanımlanan koordinat uzayı ve birimlerinde konumlandırılır.

Bir şekil, metin içinde satır içi ya da yüzen olarak konumlandırılabilir. Konumlandırma yöntemi [WrapType](./get_wraptype/) özelliği kullanılarak kontrol edilir.

Bir şekil yüzerken, bir şeye göre konumlandırılır (ör. geçerli paragraf, kenar boşluğu veya sayfa). Şeklin göreceli konumlandırması [RelativeHorizontalPosition](./get_relativehorizontalposition/) ve [RelativeVerticalPosition](./get_relativeverticalposition/) özellikleri kullanılarak belirtilir.

Yüzen bir şekil, [Left](./get_left/) ve [Top](./get_top/) özellikleri kullanılarak açıkça konumlandırılabilir veya [HorizontalAlignment](./get_horizontalalignment/) ve [VerticalAlignment](./get_verticalalignment/) özellikleri kullanılarak başka bir nesneye göre hizalanabilir.

## Örnekler



Sayfanın ortasına yüzen bir görüntünün nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Üst üste gelen metnin arkasında görünecek bir yüzen görüntü ekleyin ve sayfanın ortasına hizalayın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Ayrıca Bakınız

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
