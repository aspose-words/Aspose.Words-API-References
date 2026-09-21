---
title: "Aspose::Words::Drawing::GroupShape class"
linktitle: "GroupShape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GroupShape class. Representerar en grupp av former i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Representerar en grupp former i ett dokument. För att lära dig mer, besök dokumentationsartikeln [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/).

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka slutet av [GroupShape](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka början av [GroupShape](./). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Lägger till värden för effektutbredning till källrektangeln och returnerar den slutliga rektangeln. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Hämtar eller anger ett värde som specificerar om denna form kan överlappa andra former. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Definierar alternativ text som ska visas i stället för en grafik. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Anger om formens ankare är låst. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Anger om formens bildförhållande är låst. |
| [get_BehindText](../shapebase/get_behindtext/)() | Anger om formen är under eller över text. |
| [get_Bottom](../shapebase/get_bottom/)() | Hämtar positionen för den nedre kanten av formens innehållande block. |
| [get_Bounds](../shapebase/get_bounds/)() | Hämtar eller anger platsen och storleken på formens innehållande block. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Hämtar platsen och storleken på formens innehållande block i punkter, relativt till ankaret för den översta formen. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Hämtar den slutgiltiga omfattningen som detta formobjekt har efter att ritningseffekter har tillämpats. Värdet mäts i punkter. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Returnerar **true** om formtypen tillåter att formen har en bild. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Koordinaterna i det övre vänstra hörnet av formens innehållande block. |
| [get_CoordSize](../shapebase/get_coordsize/)() | Bredden och höjden på koordinatrymden inuti formens innehållande block. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens nedre kant. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens vänstra kant. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens högra kant. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens övre kant. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Fill](../shapebase/get_fill/)() | Hämtar fyllningsformatering för formen. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Ändrar orienteringen för en form. |
| [get_Font](../shapebase/get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| [get_Glow](../shapebase/get_glow/)() | Hämtar glödformatering för formen. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_Height](../shapebase/get_height/)() | Hämtar eller anger höjden på formens innehållande block. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Hämtar eller anger värdet som representerar procentandelen av formens relativa höjd. |
| [get_Hidden](../shapebase/get_hidden/)() | Hämtar eller anger ett booleskt värde som indikerar om formen är synlig. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Anger hur formen är placerad horisontellt. |
| [get_HRef](../shapebase/get_href/)() | Hämtar eller anger den fullständiga hyperlänkadressen för en form. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Hämtar eller anger flaggan som specificerar om formen är dekorativ i dokumentet. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Returnerar **true** om detta är en gruppform. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Returnerar **true** om denna form är en horisontell linje. |
| [get_IsImage](../shapebase/get_isimage/)() | Returnerar **true** om denna form är en bildform. |
| [get_IsInline](../shapebase/get_isinline/)() | Ett snabbt sätt att avgöra om denna form är placerad i linje med text. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Hämtar eller anger en flagga som indikerar om formen visas inuti en tabell eller utanför den. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Indikerar att formen är en [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Returnerar **true** om denna form inte är ett barn till en gruppform. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Returnerar **true** om denna form är ett WordArt-objekt. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_Left](../shapebase/get_left/)() | Hämtar eller anger positionen för den vänstra kanten av den omgivande blocket för formen. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Hämtar eller anger värdet som representerar formens relativa vänstra position i procent. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Hämtar MarkupLanguage som används för detta grafiska objekt. |
| [get_Name](../shapebase/get_name/)() | Hämtar eller anger det valfria namnet på formen. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Returnerar det omedelbara föräldra‑stycket. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_Reflection](../shapebase/get_reflection/)() | Hämtar reflektionsformatering för formen. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Anger relativt vad formen är placerad horisontellt. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Hämtar eller anger värdet för formens relativa storlek i horisontell riktning. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Anger relativt vad formen är placerad vertikalt. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Hämtar eller anger värdet för formens relativa storlek i vertikal riktning. |
| [get_Right](../shapebase/get_right/)() | Hämtar positionen för den högra kanten av det omgivande blocket för formen. |
| [get_Rotation](../shapebase/get_rotation/)() | Definierar vinkeln (i grader) som en form roteras. Positivt värde motsvarar medurs rotationsvinkel. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Definierar texten som visas när muspekaren rör sig över formen. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Hämtar skuggformatering för formen. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Hämtar formens typ. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Hämtar formens storlek i punkter. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Hämtar mjuk kantformatering för formen. |
| [get_Target](../shapebase/get_target/)() | Hämtar eller anger målramen för formens hyperlänk. |
| [get_Title](../shapebase/get_title/)() | Hämtar eller anger titeln (rubriken) för det aktuella formobjektet. |
| [get_Top](../shapebase/get_top/)() | Hämtar eller anger positionen för den övre kanten av formens omgivande block. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Hämtar eller anger värdet som representerar formens relativa topposition i procent. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Anger hur formen är placerad vertikalt. |
| [get_Width](../shapebase/get_width/)() | Hämtar eller anger bredden på formens omgivande block. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Hämtar eller anger värdet som representerar procentandelen av formens relativa bredd. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Anger hur texten flödar runt formen. |
| [get_WrapType](../shapebase/get_wraptype/)() | Definierar om formen är infogad i linjen eller flytande. För flytande former definierar den omslagstypen för text runt formen. |
| [get_ZOrder](../shapebase/get_zorder/)() | Bestämmer visningsordningen för överlappande former. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Skapar och returnerar ett objekt som kan användas för att rendera denna form till en bild. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Skapar en ny gruppform. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar indexet för den angivna barnnoden i barnnodarrayen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Konverterar ett värde från det lokala koordinatsystemet till föräldraformens koordinatsystem. |
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
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Sättare för [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Settare för [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Settare för [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Settare för [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Settare för [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Settare för [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


En [GroupShape](./) är en sammansatt nod och kan ha [Shape](../shape/) och [GroupShape](./) noder som barn.

Varje [GroupShape](./) definierar ett nytt koordinatsystem för sina underordnade former. Koordinatsystemet definieras med hjälp av egenskaperna [CoordSize](../shapebase/get_coordsize/) och [CoordOrigin](../shapebase/get_coordorigin/).

## Se även

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
