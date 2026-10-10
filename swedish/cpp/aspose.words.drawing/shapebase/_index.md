---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase class. Basisklass för objekt i ritlagret, såsom en AutoShape, fri form, OLE-objekt, ActiveX-kontroll eller bild. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


Basklass för objekt i ritlagret, såsom en AutoShape, frihandsform, OLE‑objekt, ActiveX‑kontroll eller bild. För att lära dig mer, besök dokumentationsartikeln [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

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

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepterar en besökare. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXEnd-metoden hos den angivna dokumentbesökaren. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | När den implementeras i en avledd klass, anropar den VisitXXXStart-metoden hos den angivna dokumentbesökaren. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Lägger till värden för effektutbredning till källrektangeln och returnerar den slutliga rektangeln. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_AllowOverlap](./get_allowoverlap/)() | Hämtar eller anger ett värde som specificerar om denna form kan överlappa andra former. |
| [get_AlternativeText](./get_alternativetext/)() | Definierar alternativ text som ska visas i stället för en grafik. |
| [get_AnchorLocked](./get_anchorlocked/)() | Anger om formens ankare är låst. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Anger om formens bildförhållande är låst. |
| [get_BehindText](./get_behindtext/)() | Anger om formen är under eller över text. |
| [get_Bottom](./get_bottom/)() | Hämtar positionen för den nedre kanten av formens innehållande block. |
| [get_Bounds](./get_bounds/)() | Hämtar eller anger platsen och storleken på formens innehållande block. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | Hämtar platsen och storleken på formens innehållande block i punkter, relativt till ankaret för den översta formen. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Hämtar den slutgiltiga omfattningen som detta formobjekt har efter att ritningseffekter har tillämpats. Värdet mäts i punkter. |
| [get_CanHaveImage](./get_canhaveimage/)() | Returnerar **true** om formtypen tillåter att formen har en bild. |
| [get_CoordOrigin](./get_coordorigin/)() | Koordinaterna i det övre vänstra hörnet av formens innehållande block. |
| [get_CoordSize](./get_coordsize/)() | Bredden och höjden på koordinatrymden inuti formens innehållande block. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_DistanceBottom](./get_distancebottom/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens nedre kant. |
| [get_DistanceLeft](./get_distanceleft/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens vänstra kant. |
| [get_DistanceRight](./get_distanceright/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens högra kant. |
| [get_DistanceTop](./get_distancetop/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens övre kant. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Fill](./get_fill/)() | Hämtar fyllningsformatering för formen. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FlipOrientation](./get_fliporientation/)() | Ändrar orienteringen för en form. |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| [get_Glow](./get_glow/)() | Hämtar glödformatering för formen. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_Height](./get_height/)() | Hämtar eller anger höjden på formens innehållande block. |
| [get_HeightRelative](./get_heightrelative/)() | Hämtar eller anger värdet som representerar procentandelen av formens relativa höjd. |
| [get_Hidden](./get_hidden/)() | Hämtar eller anger ett booleskt värde som indikerar om formen är synlig. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Anger hur formen är placerad horisontellt. |
| [get_HRef](./get_href/)() | Hämtar eller anger den fullständiga hyperlänkadressen för en form. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_IsDecorative](./get_isdecorative/)() | Hämtar eller anger flaggan som specificerar om formen är dekorativ i dokumentet. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsGroup](./get_isgroup/)() | Returnerar **true** om detta är en gruppform. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Returnerar **true** om denna form är en horisontell linje. |
| [get_IsImage](./get_isimage/)() | Returnerar **true** om denna form är en bildform. |
| [get_IsInline](./get_isinline/)() | Ett snabbt sätt att avgöra om denna form är placerad i linje med text. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Hämtar eller anger en flagga som indikerar om formen visas inuti en tabell eller utanför den. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsSignatureLine](./get_issignatureline/)() | Indikerar att formen är en [SignatureLine](../signatureline/). |
| [get_IsTopLevel](./get_istoplevel/)() | Returnerar **true** om denna form inte är ett barn till en gruppform. |
| [get_IsWordArt](./get_iswordart/)() | Returnerar **true** om denna form är ett WordArt-objekt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_Left](./get_left/)() | Hämtar eller anger positionen för den vänstra kanten av den omgivande blocket för formen. |
| [get_LeftRelative](./get_leftrelative/)() | Hämtar eller anger värdet som representerar formens relativa vänstra position i procent. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Hämtar MarkupLanguage som används för detta grafiska objekt. |
| [get_Name](./get_name/)() | Hämtar eller anger det valfria namnet på formen. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Hämtar typen av denna nod. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](./get_parentparagraph/)() | Returnerar det omedelbara föräldra‑stycket. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_Reflection](./get_reflection/)() | Hämtar reflektionsformatering för formen. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Anger relativt vad formen är placerad horisontellt. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Hämtar eller anger värdet för formens relativa storlek i horisontell riktning. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Anger relativt vad formen är placerad vertikalt. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Hämtar eller anger värdet för formens relativa storlek i vertikal riktning. |
| [get_Right](./get_right/)() | Hämtar positionen för den högra kanten av det omgivande blocket för formen. |
| [get_Rotation](./get_rotation/)() | Definierar vinkeln (i grader) som en form roteras. Positivt värde motsvarar medurs rotationsvinkel. |
| [get_ScreenTip](./get_screentip/)() | Definierar texten som visas när muspekaren rör sig över formen. |
| [get_ShadowFormat](./get_shadowformat/)() | Hämtar skuggformatering för formen. |
| [get_ShapeType](./get_shapetype/)() | Hämtar formens typ. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Hämtar formens storlek i punkter. |
| [get_SoftEdge](./get_softedge/)() | Hämtar mjuk kantformatering för formen. |
| [get_Target](./get_target/)() | Hämtar eller anger målramen för formens hyperlänk. |
| [get_Title](./get_title/)() | Hämtar eller anger titeln (rubriken) för det aktuella formobjektet. |
| [get_Top](./get_top/)() | Hämtar eller anger positionen för den övre kanten av formens omgivande block. |
| [get_TopRelative](./get_toprelative/)() | Hämtar eller anger värdet som representerar formens relativa topposition i procent. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Anger hur formen är placerad vertikalt. |
| [get_Width](./get_width/)() | Hämtar eller anger bredden på formens omgivande block. |
| [get_WidthRelative](./get_widthrelative/)() | Hämtar eller anger värdet som representerar procentandelen av formens relativa bredd. |
| [get_WrapSide](./get_wrapside/)() | Anger hur texten flödar runt formen. |
| [get_WrapType](./get_wraptype/)() | Definierar om formen är infogad i linjen eller flytande. För flytande former definierar den omslagstypen för text runt formen. |
| [get_ZOrder](./get_zorder/)() | Bestämmer visningsordningen för överlappande former. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetShapeRenderer](./getshaperenderer/)() | Skapar och returnerar ett objekt som kan användas för att rendera denna form till en bild. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar indexet för den angivna barnnoden i barnnodarrayen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Konverterar ett värde från det lokala koordinatsystemet till föräldraformens koordinatsystem. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla barnnoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla [SmartTag](../../aspose.words.markup/smarttag/)‑nedärvda noder för den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../../aspose.words/node/) som matchar XPath‑uttrycket. |
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Settermetod för [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


Detta är en abstrakt klass. De två avledda klasserna som du kan instansiera är [Shape](../shape/) och [GroupShape](../groupshape/).

En form är en nod i dokumentträdet.

Om formen är ett barn till ett [Paragraph](../../aspose.words/paragraph/)‑objekt, sägs formen vara \"top-level\". Top-level‑former mäts och placeras i punkter.

En form kan också förekomma som ett barn till ett [GroupShape](../groupshape/)‑objekt när flera former grupperas. Barnformer i en gruppform placeras i koordinatrymden och enheterna som definieras av egenskaperna [CoordSize](./get_coordsize/) och [CoordOrigin](./get_coordorigin/) i den överordnade gruppformen.

En form kan placeras inline med text eller flytande. Placeringstypen styrs med egenskapen [WrapType](./get_wraptype/).

När en form är flytande placeras den relativt något (t.ex. det aktuella stycket, marginalen eller sidan). Den relativa placeringen av formen anges med egenskaperna [RelativeHorizontalPosition](./get_relativehorizontalposition/) och [RelativeVerticalPosition](./get_relativeverticalposition/).

En flytande form kan placeras explicit med egenskaperna [Left](./get_left/) och [Top](./get_top/) eller justeras relativt ett annat objekt med egenskaperna [HorizontalAlignment](./get_horizontalalignment/) och [VerticalAlignment](./get_verticalalignment/).

## Exempel



Visar hur man infogar en flytande bild i sidans centrum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den till sidans centrum.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Se även

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
