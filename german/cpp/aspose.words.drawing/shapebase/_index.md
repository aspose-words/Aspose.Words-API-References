---
title: "Aspose::Words::Drawing::ShapeBase class"
linktitle: "ShapeBase"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase class. Basisklasse für Objekte in der Zeichenebene, wie ein AutoShape, Freihandform, OLE-Objekt, ActiveX-Steuerelement oder Bild. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.drawing/shapebase/
---
## ShapeBase class


Basisklasse für Objekte in der Zeichenebene, wie z. B. ein AutoShape, Freiform, OLE-Objekt, ActiveX-Steuerelement oder Bild. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

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

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Akzeptiert einen Besucher. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Wenn in einer abgeleiteten Klasse implementiert, ruft sie die VisitXXXEnd-Methode des angegebenen Dokumentenbesuchers auf. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Wenn in einer abgeleiteten Klasse implementiert, ruft sie die VisitXXXStart-Methode des angegebenen Dokumentenbesuchers auf. |
| [AdjustWithEffects](./adjustwitheffects/)(System::Drawing::RectangleF) | Fügt dem Quellrechteck die Werte des Effektbereichs hinzu und gibt das endgültige Rechteck zurück. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_AllowOverlap](./get_allowoverlap/)() | Liest oder setzt einen Wert, der angibt, ob diese Form andere Formen überlappen kann. |
| [get_AlternativeText](./get_alternativetext/)() | Definiert alternativen Text, der anstelle einer Grafik angezeigt wird. |
| [get_AnchorLocked](./get_anchorlocked/)() | Gibt an, ob der Anker der Form gesperrt ist. |
| [get_AspectRatioLocked](./get_aspectratiolocked/)() | Gibt an, ob das Seitenverhältnis der Form gesperrt ist. |
| [get_BehindText](./get_behindtext/)() | Gibt an, ob die Form unter oder über dem Text liegt. |
| [get_Bottom](./get_bottom/)() | Liest die Position der unteren Kante des umgebenden Blocks der Form. |
| [get_Bounds](./get_bounds/)() | Liest oder setzt den Ort und die Größe des umgebenden Blocks der Form. |
| [get_BoundsInPoints](./get_boundsinpoints/)() | Liest den Ort und die Größe des umgebenden Blocks der Form in Punkten, relativ zum Anker der obersten Form. |
| [get_BoundsWithEffects](./get_boundswitheffects/)() | Liest die endgültige Ausdehnung, die dieses Formobjekt nach Anwendung von Zeichnungseffekten hat. Der Wert wird in Punkten gemessen. |
| [get_CanHaveImage](./get_canhaveimage/)() | Gibt **true** zurück, wenn der Formtyp es erlaubt, dass die Form ein Bild hat. |
| [get_CoordOrigin](./get_coordorigin/)() | Die Koordinaten in der oberen linken Ecke des umgebenden Blocks dieser Form. |
| [get_CoordSize](./get_coordsize/)() | Die Breite und Höhe des Koordinatenraums innerhalb des umgebenden Blocks dieser Form. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_DistanceBottom](./get_distancebottom/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der unteren Kante der Form. |
| [get_DistanceLeft](./get_distanceleft/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der linken Kante der Form. |
| [get_DistanceRight](./get_distanceright/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der rechten Kante der Form. |
| [get_DistanceTop](./get_distancetop/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der oberen Kante der Form. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_Fill](./get_fill/)() | Liest die Füllformatierung für die Form. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FlipOrientation](./get_fliporientation/)() | Wechselt die Ausrichtung einer Form. |
| [get_Font](./get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| [get_Glow](./get_glow/)() | Liest die Leuchtformatierung für die Form. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_Height](./get_height/)() | Liest oder setzt die Höhe des umgebenden Blocks der Form. |
| [get_HeightRelative](./get_heightrelative/)() | Liest oder setzt den Wert, der den Prozentsatz der relativen Höhe der Form darstellt. |
| [get_Hidden](./get_hidden/)() | Liest oder setzt einen booleschen Wert, der angibt, ob die Form sichtbar ist. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Gibt an, wie die Form horizontal positioniert ist. |
| [get_HRef](./get_href/)() | Liest oder legt die vollständige Hyperlink-Adresse für eine Form fest. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_IsDecorative](./get_isdecorative/)() | Liest oder legt das Flag fest, das angibt, ob die Form im Dokument dekorativ ist. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsGroup](./get_isgroup/)() | Gibt **true** zurück, wenn dies eine Gruppenform ist. |
| [get_IsHorizontalRule](./get_ishorizontalrule/)() | Gibt **true** zurück, wenn diese Form eine horizontale Linie ist. |
| [get_IsImage](./get_isimage/)() | Gibt **true** zurück, wenn diese Form eine Bildform ist. |
| [get_IsInline](./get_isinline/)() | Eine schnelle Möglichkeit zu bestimmen, ob diese Form im Textfluss positioniert ist. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsLayoutInCell](./get_islayoutincell/)() | Liest oder legt ein Flag fest, das angibt, ob die Form innerhalb einer Tabelle oder außerhalb davon angezeigt wird. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsSignatureLine](./get_issignatureline/)() | Gibt an, dass die Form eine [SignatureLine](../signatureline/) ist. |
| [get_IsTopLevel](./get_istoplevel/)() | Gibt **true** zurück, wenn diese Form kein Kind einer Gruppenform ist. |
| [get_IsWordArt](./get_iswordart/)() | Gibt **true** zurück, wenn diese Form ein WordArt-Objekt ist. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_Left](./get_left/)() | Liest oder legt die Position der linken Kante des enthaltenden Blocks der Form fest. |
| [get_LeftRelative](./get_leftrelative/)() | Liest oder legt den Wert fest, der die relative linke Position der Form in Prozent darstellt. |
| [get_MarkupLanguage](./get_markuplanguage/)() const | Liest die für dieses Grafikobjekt verwendete MarkupLanguage. |
| [get_Name](./get_name/)() | Liest oder legt den optionalen Namen der Form fest. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Ermittelt den Typ dieses Knotens. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](./get_parentparagraph/)() | Gibt den unmittelbaren übergeordneten Absatz zurück. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_Reflection](./get_reflection/)() | Liest die Reflexionsformatierung für die Form. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Gibt an, relativ zu welchem Element die Form horizontal positioniert ist. |
| [get_RelativeHorizontalSize](./get_relativehorizontalsize/)() | Liest oder legt den Wert der relativen Größe der Form in horizontaler Richtung fest. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Gibt an, relativ zu welchem Element die Form vertikal positioniert ist. |
| [get_RelativeVerticalSize](./get_relativeverticalsize/)() | Liest oder legt den Wert der relativen Größe der Form in vertikaler Richtung fest. |
| [get_Right](./get_right/)() | Liest die Position der rechten Kante des enthaltenden Blocks der Form. |
| [get_Rotation](./get_rotation/)() | Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem im Uhrzeigersinn gedrehten Winkel. |
| [get_ScreenTip](./get_screentip/)() | Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird. |
| [get_ShadowFormat](./get_shadowformat/)() | Ruft die Schattierungsformatierung für die Form ab. |
| [get_ShapeType](./get_shapetype/)() | Ruft den Formtyp ab. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Ruft die Größe der Form in Punkten ab. |
| [get_SoftEdge](./get_softedge/)() | Ruft die Weichkantformatierung für die Form ab. |
| [get_Target](./get_target/)() | Ruft das Ziel-Frame für den Form-Hyperlink ab oder legt es fest. |
| [get_Title](./get_title/)() | Ruft den Titel (Beschriftung) des aktuellen Formobjekts ab oder legt ihn fest. |
| [get_Top](./get_top/)() | Ruft die Position der oberen Kante des enthaltenden Blocks der Form ab oder legt sie fest. |
| [get_TopRelative](./get_toprelative/)() | Ruft den Wert ab, der die relative obere Position der Form in Prozent darstellt, oder legt ihn fest. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Gibt an, wie die Form vertikal positioniert wird. |
| [get_Width](./get_width/)() | Ruft die Breite des enthaltenden Blocks der Form ab oder legt sie fest. |
| [get_WidthRelative](./get_widthrelative/)() | Ruft den Wert ab, der den Prozentsatz der relativen Breite der Form darstellt, oder legt ihn fest. |
| [get_WrapSide](./get_wrapside/)() | Gibt an, wie der Text um die Form herumfließt. |
| [get_WrapType](./get_wraptype/)() | Definiert, ob die Form inline oder schwebend ist. Für schwebende Formen definiert es den Umbruchmodus für Text um die Form. |
| [get_ZOrder](./get_zorder/)() | Bestimmt die Anzeigereihenfolge überlappender Formen. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetShapeRenderer](./getshaperenderer/)() | Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Form in ein Bild zu rendern. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](./localtoparent/)(System::Drawing::PointF) | Konvertiert einen Wert vom lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Wählt das erste [Node](../../aspose.words/node/), das dem XPath-Ausdruck entspricht. |
| [set_AllowOverlap](./set_allowoverlap/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](./get_allowoverlap/). |
| [set_AlternativeText](./set_alternativetext/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](./get_alternativetext/). |
| [set_AnchorLocked](./set_anchorlocked/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](./get_anchorlocked/). |
| [set_AspectRatioLocked](./set_aspectratiolocked/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](./get_aspectratiolocked/). |
| [set_BehindText](./set_behindtext/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_BehindText](./get_behindtext/). |
| [set_Bounds](./set_bounds/)(System::Drawing::RectangleF) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Bounds](./get_bounds/). |
| [set_CoordOrigin](./set_coordorigin/)(System::Drawing::Point) | Setter für [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](./get_coordorigin/). |
| [set_CoordSize](./set_coordsize/)(System::Drawing::Size) | Setter für [Aspose::Words::Drawing::ShapeBase::get_CoordSize](./get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](./get_distancetop/). |
| [set_FlipOrientation](./set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Setter für [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](./get_fliporientation/). |
| [set_Height](./set_height/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Height](./get_height/). |
| [set_HeightRelative](./set_heightrelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](./get_heightrelative/). |
| [set_Hidden](./set_hidden/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Hidden](./get_hidden/). |
| [set_HorizontalAlignment](./set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter für [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](./get_horizontalalignment/). |
| [set_HRef](./set_href/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_HRef](./get_href/). |
| [set_IsDecorative](./set_isdecorative/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](./get_isdecorative/). |
| [set_IsLayoutInCell](./set_islayoutincell/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](./get_islayoutincell/). |
| [set_Left](./set_left/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Left](./get_left/). |
| [set_LeftRelative](./set_leftrelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](./get_leftrelative/). |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](./set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](./set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](./get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](./set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](./get_relativeverticalposition/). |
| [set_RelativeVerticalSize](./set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](./get_relativeverticalsize/). |
| [set_Rotation](./set_rotation/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Rotation](./get_rotation/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](./get_screentip/). |
| [set_Target](./set_target/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Target](./get_target/). |
| [set_Title](./set_title/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Title](./get_title/). |
| [set_Top](./set_top/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Top](./get_top/). |
| [set_TopRelative](./set_toprelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_TopRelative](./get_toprelative/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Setter für [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](./get_verticalalignment/). |
| [set_Width](./set_width/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Width](./get_width/). |
| [set_WidthRelative](./set_widthrelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](./get_widthrelative/). |
| [set_WrapSide](./set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Setter für [Aspose::Words::Drawing::ShapeBase::get_WrapSide](./get_wrapside/). |
| [set_WrapType](./set_wraptype/)(Aspose::Words::Drawing::WrapType) | Setter für [Aspose::Words::Drawing::ShapeBase::get_WrapType](./get_wraptype/). |
| [set_ZOrder](./set_zorder/)(int32_t) | Setter für [Aspose::Words::Drawing::ShapeBase::get_ZOrder](./get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Dies ist eine abstrakte Klasse. Die beiden abgeleiteten Klassen, die Sie instanziieren können, sind [Shape](../shape/) und [GroupShape](../groupshape/).

Ein Shape ist ein Knoten im Dokumentbaum.

Wenn das Shape ein Kind eines [Paragraph](../../aspose.words/paragraph/) Objekts ist, wird das Shape als "top-level" bezeichnet. Top-level Shapes werden in Punkten gemessen und positioniert.

Ein Shape kann auch als Kind eines [GroupShape](../groupshape/) Objekts auftreten, wenn mehrere Shapes gruppiert werden. Kind-Shapes einer Gruppierung werden im Koordinatenraum und in den Einheiten positioniert, die durch die Eigenschaften [CoordSize](./get_coordsize/) und [CoordOrigin](./get_coordorigin/) des übergeordneten GroupShape definiert sind.

Ein Shape kann inline mit Text oder schwebend positioniert werden. Die Positionierungsmethode wird über die Eigenschaft [WrapType](./get_wraptype/) gesteuert.

Wenn ein Shape schwebend ist, wird es relativ zu etwas positioniert (z. B. dem aktuellen Absatz, dem Rand oder der Seite). Die relative Positionierung des Shapes wird über die Eigenschaften [RelativeHorizontalPosition](./get_relativehorizontalposition/) und [RelativeVerticalPosition](./get_relativeverticalposition/) angegeben.

Ein schwebendes Shape kann explizit über die Eigenschaften [Left](./get_left/) und [Top](./get_top/) positioniert oder relativ zu einem anderen Objekt über die Eigenschaften [HorizontalAlignment](./get_horizontalalignment/) und [VerticalAlignment](./get_verticalalignment/) ausgerichtet werden.

## Beispiele



Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint und es an der Seitenmitte ausrichtet.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Siehe auch

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
