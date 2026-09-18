---
title: "Aspose::Words::Drawing::Shape class"
linktitle: "Shape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Shape class. Stellt ein Objekt in der Zeichenebene dar, wie z.B. ein AutoShape, Textfeld, Freiform, OLE-Objekt, ActiveX-Steuerelement oder Bild. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.drawing/shape/
---
## Shape class


Stellt ein Objekt in der Zeichenebene dar, z. B. eine AutoShape, ein Textfeld, ein Freiformobjekt, ein OLE-Objekt, ein ActiveX-Steuerelement oder ein Bild. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class Shape : public Aspose::Words::Drawing::ShapeBase,
              public Aspose::Words::Drawing::Core::ITextBox,
              public Aspose::Words::Drawing::Core::IStrokable
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende der Form zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Anfang der Form zu besuchen. |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Fügt dem Quellrechteck die Werte des Effektbereichs hinzu und gibt das endgültige Rechteck zurück. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_Adjustments](./get_adjustments/)() | Stellt Zugriff auf die Rohwerte der Anpassungen einer Form bereit. Für eine Form, die keine Rohwerte für Anpassungen enthält, wird eine leere Sammlung zurückgegeben. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Liest oder setzt einen Wert, der angibt, ob diese Form andere Formen überlappen kann. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Definiert alternativen Text, der anstelle einer Grafik angezeigt wird. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Gibt an, ob der Anker der Form gesperrt ist. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Gibt an, ob das Seitenverhältnis der Form gesperrt ist. |
| [get_BehindText](../shapebase/get_behindtext/)() | Gibt an, ob die Form unter oder über dem Text liegt. |
| [get_Bottom](../shapebase/get_bottom/)() | Liest die Position der unteren Kante des umgebenden Blocks der Form. |
| [get_Bounds](../shapebase/get_bounds/)() | Liest oder setzt den Ort und die Größe des umgebenden Blocks der Form. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Liest den Ort und die Größe des umgebenden Blocks der Form in Punkten, relativ zum Anker der obersten Form. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Liest die endgültige Ausdehnung, die dieses Formobjekt nach Anwendung von Zeichnungseffekten hat. Der Wert wird in Punkten gemessen. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Gibt **true** zurück, wenn der Formtyp es erlaubt, dass die Form ein Bild hat. |
| [get_Chart](./get_chart/)() | Bietet Zugriff auf die Diagrammeigenschaften, wenn diese Form ein [Chart](../../aspose.words.drawing.charts/chart/) enthält. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | Die Koordinaten in der oberen linken Ecke des umgebenden Blocks dieser Form. |
| [get_CoordSize](../shapebase/get_coordsize/)() | Die Breite und Höhe des Koordinatenraums innerhalb des umgebenden Blocks dieser Form. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der unteren Kante der Form. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der linken Kante der Form. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der rechten Kante der Form. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Liest oder setzt den Abstand (in Punkten) zwischen dem Dokumenttext und der oberen Kante der Form. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_ExtrusionEnabled](./get_extrusionenabled/)() | Gibt **true** zurück, wenn ein Extrusionseffekt aktiviert ist. |
| [get_Fill](../shapebase/get_fill/)() | Liest die Füllformatierung für die Form. |
| [get_FillColor](./get_fillcolor/)() | Definiert die Pinsel‑Farbe, die den geschlossenen Pfad der Form füllt. |
| [get_Filled](./get_filled/)() | Bestimmt, ob der geschlossene Pfad der Form gefüllt wird. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FirstParagraph](./get_firstparagraph/)() | Liefert den ersten Absatz in der Form. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Wechselt die Ausrichtung einer Form. |
| [get_Font](../shapebase/get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| [get_Glow](../shapebase/get_glow/)() | Liest die Leuchtformatierung für die Form. |
| [get_HasChart](./get_haschart/)() | Gibt **true** zurück, wenn diese [Shape](./) ein [Chart](../../aspose.words.drawing.charts/chart/) hat. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_HasImage](./get_hasimage/)() | Gibt **true** zurück, wenn die shape Bildbytes enthält oder ein Bild verlinkt. |
| [get_HasSmartArt](./get_hassmartart/)() | Gibt **true** zurück, wenn diese [Shape](./) ein SmartArt‑Objekt hat. |
| [get_Height](../shapebase/get_height/)() | Liest oder setzt die Höhe des umgebenden Blocks der Form. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Liest oder setzt den Wert, der den Prozentsatz der relativen Höhe der Form darstellt. |
| [get_Hidden](../shapebase/get_hidden/)() | Liest oder setzt einen booleschen Wert, der angibt, ob die Form sichtbar ist. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Gibt an, wie die Form horizontal positioniert ist. |
| [get_HorizontalRuleFormat](./get_horizontalruleformat/)() | Bietet Zugriff auf die Eigenschaften der horizontalen Linienform. Für eine Form, die keine horizontale Linie ist, wird **null** zurückgegeben. |
| [get_HRef](../shapebase/get_href/)() | Liest oder legt die vollständige Hyperlink-Adresse für eine Form fest. |
| [get_ImageData](./get_imagedata/)() | Bietet Zugriff auf das Bild der Form. Gibt **null** zurück, wenn die Form kein Bild haben kann. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Liest oder legt das Flag fest, das angibt, ob die Form im Dokument dekorativ ist. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Gibt **true** zurück, wenn dies eine Gruppenform ist. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Gibt **true** zurück, wenn diese Form eine horizontale Linie ist. |
| [get_IsImage](../shapebase/get_isimage/)() | Gibt **true** zurück, wenn diese Form eine Bildform ist. |
| [get_IsInline](../shapebase/get_isinline/)() | Eine schnelle Möglichkeit zu bestimmen, ob diese Form im Textfluss positioniert ist. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Liest oder legt ein Flag fest, das angibt, ob die Form innerhalb einer Tabelle oder außerhalb davon angezeigt wird. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Gibt an, dass die Form eine [SignatureLine](../signatureline/) ist. |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Gibt **true** zurück, wenn diese Form kein Kind einer Gruppenform ist. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Gibt **true** zurück, wenn diese Form ein WordArt-Objekt ist. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_LastParagraph](./get_lastparagraph/)() | Liefert den letzten Absatz in der Form. |
| [get_Left](../shapebase/get_left/)() | Liest oder legt die Position der linken Kante des enthaltenden Blocks der Form fest. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Liest oder legt den Wert fest, der die relative linke Position der Form in Prozent darstellt. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Liest die für dieses Grafikobjekt verwendete MarkupLanguage. |
| [get_Name](../shapebase/get_name/)() | Liest oder legt den optionalen Namen der Form fest. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [Shape](../../aspose.words/nodetype/) zurück. |
| [get_OleFormat](./get_oleformat/)() | Bietet Zugriff auf die OLE‑Daten einer Form. Für eine Form, die kein OLE‑Objekt oder ActiveX‑Steuerelement ist, wird **null** zurückgegeben. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Gibt den unmittelbaren übergeordneten Absatz zurück. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_Reflection](../shapebase/get_reflection/)() | Liest die Reflexionsformatierung für die Form. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Gibt an, relativ zu welchem Element die Form horizontal positioniert ist. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Liest oder legt den Wert der relativen Größe der Form in horizontaler Richtung fest. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Gibt an, relativ zu welchem Element die Form vertikal positioniert ist. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Liest oder legt den Wert der relativen Größe der Form in vertikaler Richtung fest. |
| [get_Right](../shapebase/get_right/)() | Liest die Position der rechten Kante des enthaltenden Blocks der Form. |
| [get_Rotation](../shapebase/get_rotation/)() | Definiert den Winkel (in Grad), um den eine Form gedreht wird. Ein positiver Wert entspricht einem im Uhrzeigersinn gedrehten Winkel. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird. |
| [get_ShadowEnabled](./get_shadowenabled/)() | Gibt **true** zurück, wenn ein Schatteneffekt aktiviert ist. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Ruft die Schattierungsformatierung für die Form ab. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Ruft den Formtyp ab. |
| [get_SignatureLine](./get_signatureline/)() | Liefert das [SignatureLine](../signatureline/)-Objekt, wenn die Form eine Signaturzeile ist. Gibt sonst **null** zurück. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Ruft die Größe der Form in Punkten ab. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Ruft die Weichkantformatierung für die Form ab. |
| [get_StoryType](./get_storytype/)() | Gibt [Textbox](../../aspose.words/storytype/) zurück. |
| [get_Stroke](./get_stroke/)() | Definiert einen Strich für eine Form. |
| [get_StrokeColor](./get_strokecolor/)() | Definiert die Farbe eines Strichs. |
| [get_Stroked](./get_stroked/)() | Definiert, ob der Pfad gestrichen wird. |
| [get_StrokeWeight](./get_strokeweight/)() | Definiert die Pinselstärke, mit der der Pfad einer Form in Punkten gestrichen wird. |
| [get_Target](../shapebase/get_target/)() | Ruft das Ziel-Frame für den Form-Hyperlink ab oder legt es fest. |
| [get_TextBox](./get_textbox/)() | Definiert Attribute, die festlegen, wie Text in einer Form angezeigt wird. |
| [get_TextPath](./get_textpath/)() | Definiert den Text des Textpfads (eines WordArt‑Objekts). |
| [get_Title](../shapebase/get_title/)() | Ruft den Titel (Beschriftung) des aktuellen Formobjekts ab oder legt ihn fest. |
| [get_Top](../shapebase/get_top/)() | Ruft die Position der oberen Kante des enthaltenden Blocks der Form ab oder legt sie fest. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Ruft den Wert ab, der die relative obere Position der Form in Prozent darstellt, oder legt ihn fest. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Gibt an, wie die Form vertikal positioniert wird. |
| [get_Width](../shapebase/get_width/)() | Ruft die Breite des enthaltenden Blocks der Form ab oder legt sie fest. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Ruft den Wert ab, der den Prozentsatz der relativen Breite der Form darstellt, oder legt ihn fest. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Gibt an, wie der Text um die Form herumfließt. |
| [get_WrapType](../shapebase/get_wraptype/)() | Definiert, ob die Form inline oder schwebend ist. Für schwebende Formen definiert es den Umbruchmodus für Text um die Form. |
| [get_ZOrder](../shapebase/get_zorder/)() | Bestimmt die Anzeigereihenfolge überlappender Formen. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Form in ein Bild zu rendern. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Konvertiert einen Wert vom lokalen Koordinatenraum in den Koordinatenraum der übergeordneten Form. |
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
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Setter für [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Setter für [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FillColor](./set_fillcolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::Shape::get_FillColor](./get_fillcolor/). |
| [set_Filled](./set_filled/)(bool) | Setter für [Aspose::Words::Drawing::Shape::get_Filled](./get_filled/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Setter für [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_HeightRelative](../shapebase/get_heightrelative/). |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Hidden](../shapebase/get_hidden/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter für [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Setter für [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_LeftRelative](../shapebase/get_leftrelative/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Setter für [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_StrokeColor](./set_strokecolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::Shape::get_StrokeColor](./get_strokecolor/). |
| [set_Stroked](./set_stroked/)(bool) | Setter für [Aspose::Words::Drawing::Shape::get_Stroked](./get_stroked/). |
| [set_StrokeWeight](./set_strokeweight/)(double) | Setter für [Aspose::Words::Drawing::Shape::get_StrokeWeight](./get_strokeweight/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_TopRelative](../shapebase/get_toprelative/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Setter für [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Setter für [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Setter für [Aspose::Words::Drawing::ShapeBase::get_WidthRelative](../shapebase/get_widthrelative/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Setter für [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Setter für [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Setter für [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Shape](./shape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Drawing::ShapeType) | Erstellt ein neues Form‑Objekt. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
| [UpdateSmartArtDrawing](./updatesmartartdrawing/)() | Aktualisiert die vorgerenderte SmartArt‑Zeichnung mithilfe der SmartArt‑Cold‑Rendering‑Engine von [Aspose.Words](../../aspose.words/). |
## Hinweise


Mit der [Shape](./)-Klasse können Sie Formen in einem Microsoft‑Word‑Dokument erstellen oder ändern.

Eine wichtige Eigenschaft einer Form ist ihr [ShapeType](../shapebase/get_shapetype/). Formen verschiedener Typen können unterschiedliche Fähigkeiten in einem Word‑Dokument haben. Zum Beispiel können nur Bild‑ und OLE‑Formen Bilder in sich enthalten. Die meisten Formen können Text enthalten, jedoch nicht alle.

Formen, die Text enthalten können, können [Paragraph](../../aspose.words/paragraph/)- und [Table](../../aspose.words.tables/table/)-Knoten als Kinder enthalten.

## Beispiele



Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Holen Sie die Sammlung von Formen aus dem Dokument,
// und speichern Sie die Bilddaten jeder Form, die ein Bild enthält, als Datei im lokalen Dateisystem.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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


Zeigt, wie man alle Formen aus einem Dokument löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie zwei Formen zusammen mit einer Gruppierungsform ein, die eine weitere Form enthält.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 400, 200);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Star, 300, 300);

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 50.0f, 200.0f, 100.0f));
group->set_CoordOrigin(System::Drawing::Point(-1000, -500));

auto subShape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
subShape->set_Width(500);
subShape->set_Height(700);
subShape->set_Left(0);
subShape->set_Top(0);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(subShape);
builder->InsertNode(group);

ASSERT_EQ(3, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true)->get_Count());

// Entfernen Sie alle Shape‑Knoten aus dem Dokument.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
shapes->Clear();

// Alle Formen sind entfernt, aber die Gruppierungsform ist weiterhin im Dokument.
ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true)->get_Count());
ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Entfernen Sie alle Gruppierungsformen einzeln.
System::SharedPtr<Aspose::Words::NodeCollection> groupShapes = doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true);
groupShapes->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::GroupShape, true)->get_Count());
ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Siehe auch

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
