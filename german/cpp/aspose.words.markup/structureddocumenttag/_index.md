---
title: "Aspose::Words::Markup::StructuredDocumentTag Klasse"
linktitle: "StructuredDocumentTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag Klasse. Stellt ein strukturiertes Dokument‑Tag (SDT oder Inhaltssteuerelement) in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Stellt einen strukturierten Dokumenttag (SDT oder Inhaltssteuerelement) in einem Dokument dar. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende des [StructuredDocumentTag](./) zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Anfang des [StructuredDocumentTag](./) zu besuchen. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Löscht den Inhalt dieses strukturierten Dokument‑Tags und zeigt einen Platzhalter an, falls er definiert ist. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_Appearance](./get_appearance/)() override | Liest/legt das Erscheinungsbild eines strukturierten Dokument‑Tags fest. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Gibt die Kategorie des Bausteins für diesen **SDT**‑Knoten an. Darf nicht **null** sein. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Gibt den Typ des Bausteins für dieses **SDT** an. Darf nicht **null** sein. |
| [get_CalendarType](./get_calendartype/)() | Gibt den Kalendertyp für dieses **SDT** an. Standard ist [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Liest/legt den aktuellen Zustand der Checkbox **SDT** fest. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_Color](./get_color/)() override | Liest oder setzt die Farbe des strukturierten Dokument-Tags. |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) Formatierung, die auf Text angewendet wird, der in **SDT** eingegeben wird. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Zeichenkette, die das Format darstellt, in dem Daten angezeigt werden. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Ermöglicht das Setzen/Auslesen des Sprachformats für das in diesem **SDT** angezeigte Datum. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Liest/legt das Format fest, in dem das Datum für ein Datums‑SDT gespeichert wird, wenn das **SDT** an einen XML‑Knoten im Datenspeicher des Dokuments gebunden ist. Der Standardwert ist [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) Formatierung, die auf das letzte Zeichen des in das **SDT** eingegebenen Textes angewendet wird. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FullDate](./get_fulldate/)() | Gibt das zuletzt in dieses **SDT** eingegebene vollständige Datum und die Uhrzeit an. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_Id](./get_id/)() override | Gibt eine eindeutige schreibgeschützte persistente numerische Id für dieses **SDT** an. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Gibt an, ob der Inhalt dieses **SDT** als Platzhaltertext interpretiert werden soll (im Gegensatz zu regulärem Textinhalt im SDT). Wenn auf **true** gesetzt, wird dieser Zustand beim Öffnen des Dokuments wiederhergestellt (Platzhaltertext wird angezeigt). |
| [get_IsTemporary](./get_istemporary/)() const | Gibt an, ob dieses **SDT** aus dem WordProcessingML‑Dokument entfernt werden soll, wenn sein Inhalt geändert wird. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_Level](./get_level/)() const override | Liest die Ebene, auf der dieses **SDT** im Dokumentbaum vorkommt. |
| [get_ListItems](./get_listitems/)() | Liest die mit diesem **SDT** verbundene [SdtListItemCollection](../sdtlistitemcollection/). |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Wenn auf **true** gesetzt, verhindert diese Eigenschaft, dass ein Benutzer dieses **SDT** löscht. |
| [get_LockContents](./get_lockcontents/)() override | Wenn auf **true** gesetzt, verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieses **SDT** bearbeitet. |
| [get_Multiline](./get_multiline/)() | Gibt an, ob dieses **SDT** mehrere Textzeilen zulässt. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [StructuredDocumentTag](../../aspose.words/nodetype/) zurück. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_Placeholder](./get_placeholder/)() override | Liest das [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), das Platzhaltertext enthält und angezeigt werden soll, wenn der Inhalt dieses SDT‑Laufs leer ist, das zugehörige zugeordnete XML‑Element leer ist, wie über das [XmlMapping](./get_xmlmapping/)‑Element angegeben, oder das [IsShowingPlaceholderText](./get_isshowingplaceholdertext/)‑Element **true** ist. |
| [get_PlaceholderName](./get_placeholdername/)() override | Liest oder setzt den Namen des [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), das Platzhaltertext enthält. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_SdtType](./get_sdttype/)() override | Liest den Typ dieses **Structured document tag**. |
| [get_Style](./get_style/)() | Liest oder legt den [Style](../../aspose.words/style/) des strukturierten Dokumenttags fest. |
| [get_StyleName](./get_stylename/)() | Liest oder legt den Namen des auf den strukturierten Dokumenttag angewendeten Stils fest. |
| [get_Tag](./get_tag/)() const override | Gibt ein Tag an, das dem aktuellen SDT‑Knoten zugeordnet ist. Darf nicht **null** sein. |
| [get_Title](./get_title/)() const override | Gibt den benutzerfreundlichen Namen an, der mit diesem **SDT** verknüpft ist. Darf nicht **null** sein. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Liest einen String, der das XML darstellt, das im Knoten im [FlatOpc](../../aspose.words/saveformat/)‑Format enthalten ist. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Liest einen String, der das im Knoten enthaltene XML im [FlatOpc](../../aspose.words/saveformat/)-Format darstellt. Im Gegensatz zur [WordOpenXML](./get_wordopenxml/)-Eigenschaft erzeugt diese Methode ein vereinfachtes Dokument, das alle nicht inhaltbezogenen Teile ausschließt. |
| [get_XmlMapping](./get_xmlmapping/)() override | Liest ein Objekt, das die Zuordnung dieses strukturierten Dokument-Tags zu XML‑Daten in einem benutzerdefinierten XML‑Teil des aktuellen Dokuments darstellt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Entfernt nur diesen SDT‑Knoten selbst, lässt jedoch den Inhalt im Dokumentbaum erhalten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../smarttag/)-Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Wählt das erste [Node](../../aspose.words/node/), das dem XPath-Ausdruck entspricht. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Setter für [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Legt das Symbol fest, das verwendet wird, um den aktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements darzustellen. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Legt das Symbol fest, das verwendet wird, um den deaktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements darzustellen. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Initialisiert eine neue Instanz der Klasse **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Strukturierte Dokument‑Tags (SDTs) ermöglichen das Einbetten von kundenspezifischer Semantik sowie deren Verhalten und Aussehen in ein Dokument.

In dieser Version bietet Aspose.Words eine Reihe öffentlicher Methoden und Eigenschaften, um das Verhalten und den Inhalt von [StructuredDocumentTag](./) zu manipulieren. Die Zuordnung von SDT‑Knoten zu benutzerdefinierten XML‑Paketen innerhalb eines Dokuments kann mithilfe der [XmlMapping](./get_xmlmapping/)‑Eigenschaft durchgeführt werden.

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Beispiele



Zeigt, wie man mit Stilen für Content-Control-Elemente arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Möglichkeiten aufgeführt, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 -  Wende ein Stilobjekt aus der Stilsammlung des Dokuments an:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Verweise im Dokument per Name auf einen Stil:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## Siehe auch

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
