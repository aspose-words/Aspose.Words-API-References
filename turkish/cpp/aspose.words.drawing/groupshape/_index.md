---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::GroupShape sınıfı. Bir belgede şekiller grubunu temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Bir belgede şekil grubunu temsil eder. Daha fazla bilgi için, [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi, [GroupShape](./) sonunu ziyaret etmek için kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi, [GroupShape](./) başlangıcını ziyaret etmek için kabul eder. |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Kaynak dikdörtgene etki genişliğinin değerlerini ekler ve son dikdörtgeni döndürür. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Bu şeklin diğer şekillerin üzerine çıkıp çıkamayacağını belirten bir değeri alır veya ayarlar. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Grafik yerine gösterilecek alternatif metni tanımlar. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Şeklin çapa noktasının kilitli olup olmadığını belirtir. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Şeklin en‑boy oranının kilitli olup olmadığını belirtir. |
| [get_BehindText](../shapebase/get_behindtext/)() | Şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir. |
| [get_Bottom](../shapebase/get_bottom/)() | Şeklin içinde bulunduğu bloğun alt kenar konumunu alır. |
| [get_Bounds](../shapebase/get_bounds/)() | Şeklin içinde bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | En üst şeklin çapa noktasına göre, şeklin içinde bulunduğu bloğun konumunu ve boyutunu nokta cinsinden alır. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son kapsamı alır. Değer nokta cinsinden ölçülür. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Şekil türü şeklin bir görüntüye sahip olmasına izin veriyorsa **true** döndürür. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Bu şeklin içinde bulunduğu bloğun sol üst köşesindeki koordinatlar. |
| [get_CoordSize](../shapebase/get_coordsize/)() | Bu şeklin içinde bulunduğu bloğun içindeki koordinat alanının genişliği ve yüksekliği. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Belge metni ile şeklin alt kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Belge metni ile şeklin sol kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Belge metni ile şeklin sağ kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_Fill](../shapebase/get_fill/)() | Şekil için dolgu biçimlendirmesini alır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Bir şeklin yönünü değiştirir. |
| [get_Font](../shapebase/get_font/)() | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Glow](../shapebase/get_glow/)() | Şekil için parıltı biçimlendirmesini alır. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_Height](../shapebase/get_height/)() | Şeklin içinde bulunduğu bloğun yüksekliğini alır veya ayarlar. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Şeklin göreceli yüksekliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [get_Hidden](../shapebase/get_hidden/)() | Şeklin görünür olup olmadığını gösteren bir boolean değeri alır veya ayarlar. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Şeklin yatay olarak nasıl konumlandırıldığını belirtir. |
| [get_HRef](../shapebase/get_href/)() | Bir şekil için tam hiperlink adresini alır veya ayarlar. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Şeklin belgede dekoratif olup olmadığını belirten bayrağı alır veya ayarlar. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Bu bir grup şekil ise **true** döndürür. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Bu şekil bir yatay kural ise **true** döndürür. |
| [get_IsImage](../shapebase/get_isimage/)() | Bu şekil bir resim şekli ise **true** döndürür. |
| [get_IsInline](../shapebase/get_isinline/)() | Bu şeklin metin içinde satır içi konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de eklenmişse true döndürür. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Şeklin bir tablo içinde mi yoksa dışında mı görüntülendiğini gösteren bayrağı alır veya ayarlar. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (eklenmiş) ise **true** döndürür. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Şeklin bir [SignatureLine](../signatureline/) olduğunu gösterir. |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Bu şekil bir grup şeklin çocuğu değilse **true** döndürür. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Bu şekil bir WordArt nesnesi ise **true** döndürür. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_Left](../shapebase/get_left/)() | Şeklin içinde bulunduğu bloğun sol kenar konumunu alır veya ayarlar. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Şeklin yüzde olarak göreceli sol konumunu temsil eden değeri alır veya ayarlar. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Bu grafik nesnesi için kullanılan MarkupLanguage'ı alır. |
| [get_Name](../shapebase/get_name/)() | İsteğe bağlı şekil adını alır veya ayarlar. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [GroupShape](../../aspose.words/nodetype/) döndürür. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Doğrudan üst paragrafı döndürür. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_Reflection](../shapebase/get_reflection/)() | Şekil için yansıma biçimlendirmesini alır. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Şeklin yatay olarak neye göre konumlandırıldığını belirtir. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Şeklin yatay yönde göreceli boyut değerini alır veya ayarlar. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Şeklin dikey olarak neye göre konumlandırıldığını belirtir. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Şeklin dikey yönde göreceli boyut değerini alır veya ayarlar. |
| [get_Right](../shapebase/get_right/)() | Şeklin içinde bulunduğu bloğun sağ kenar konumunu alır. |
| [get_Rotation](../shapebase/get_rotation/)() | Bir şeklin döndürüldüğü açıyı (derece cinsinden) tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Fare işaretçisi şeklin üzerine hareket ettiğinde gösterilen metni tanımlar. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Şekil için gölge biçimlendirmesini alır. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Şekil tipini alır. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Şeklin boyutunu puan cinsinden alır. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Şekil için yumuşak kenar biçimlendirmesini alır. |
| [get_Target](../shapebase/get_target/)() | Şekil bağlantısı için hedef çerçeveyi alır veya ayarlar. |
| [get_Title](../shapebase/get_title/)() | Mevcut şekil nesnesinin başlığını (alt yazısını) alır veya ayarlar. |
| [get_Top](../shapebase/get_top/)() | Şeklin içinde bulunduğu bloğun üst kenar konumunu alır veya ayarlar. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Şeklin yüzde cinsinden göreceli üst konumunu temsil eden değeri alır veya ayarlar. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Şeklin dikey olarak nasıl konumlandırıldığını belirtir. |
| [get_Width](../shapebase/get_width/)() | Şeklin içinde bulunduğu bloğun genişliğini alır veya ayarlar. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Şeklin göreceli genişliğinin yüzdesini temsil eden değeri alır veya ayarlar. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Metnin şeklin etrafında nasıl kaydırıldığını belirtir. |
| [get_WrapType](../shapebase/get_wraptype/)() | Şeklin satır içinde mi yoksa yüzen mi olduğunu tanımlar. Yüzen şekiller için metnin şeklin etrafındaki kaydırma modunu tanımlar. |
| [get_ZOrder](../shapebase/get_zorder/)() | Üst üste binen şekillerin görüntüleme sırasını belirler. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Bu şekli bir görüntüye renderlemek için kullanılabilecek bir nesne oluşturur ve döndürür. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Yeni bir grup şekli oluşturur. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Bir değeri yerel koordinat alanından üst şeklin koordinat alanına dönüştürür. |
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
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir [GroupShape](./) birleşik bir düğümdür ve alt öğe olarak [Shape](../shape/) ve [GroupShape](./) düğümlerine sahip olabilir.

Her [GroupShape](./) çocuk şekilleri için yeni bir koordinat sistemi tanımlar. Koordinat sistemi, [CoordSize](../shapebase/get_coordsize/) ve [CoordOrigin](../shapebase/get_coordorigin/) özellikleri kullanılarak tanımlanır.

## Ayrıca Bakınız

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
