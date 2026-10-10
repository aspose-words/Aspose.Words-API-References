---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart Klasse"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart Klasse. Stellt den Beginn eines bereichsbezogenen strukturierten Dokument-Tags dar, das mehrseitigen Inhalt akzeptiert. Siehe auch StructuredDocumentTagRangeEnd. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Stellt den Beginn eines **ranged** strukturierten Dokument-Tags dar, das mehrseitigen Inhalt akzeptiert. Siehe auch [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). Weitere Informationen finden Sie im Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt den angegebenen Knoten am Ende des stdContent-Bereichs hinzu. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_Appearance](./get_appearance/)() override | Liest oder setzt das Erscheinungsbild des strukturierten Dokument-Tags. |
| [get_Color](./get_color/)() override | Liest oder setzt die Farbe des strukturierten Dokument-Tags. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_Id](./get_id/)() override | Gibt eine eindeutige schreibgeschützte persistente numerische Id für dieses strukturierte Dokument-Tag an. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Liefert **true**, wenn dieser Knoten andere Knoten enthalten kann. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Gibt an, ob der Inhalt dieses strukturierten Dokument-Tags als Platzhaltertext interpretiert werden soll (im Gegensatz zu regulärem Textinhalt innerhalb des strukturierten Dokument-Tags). Wenn auf **true** gesetzt, wird dieser Zustand beim Öffnen des Dokuments wiederhergestellt (Platzhaltertext wird angezeigt). |
| [get_LastChild](./get_lastchild/)() | Gibt das letzte untergeordnete Element im stdContent-Bereich zurück. |
| [get_Level](./get_level/)() const override | Gibt die Ebene zurück, auf der dieser Start des strukturierten Dokument-Tag-Bereichs im Dokumentbaum auftritt. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Wenn auf **true** gesetzt, verhindert diese Eigenschaft, dass ein Benutzer dieses strukturierte Dokument-Tag löscht. |
| [get_LockContents](./get_lockcontents/)() override | Wenn auf **true** gesetzt, verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieses strukturierten Dokument-Tags bearbeitet. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/) zurück. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_Placeholder](./get_placeholder/)() override | Ruft das [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) ab, das Platzhaltertext enthält, der angezeigt werden soll, wenn der Inhalt dieses strukturierten Dokumenten‑Tags leer ist, das zugeordnete gemappte XML‑Element ist leer, wie über das [XmlMapping](./get_xmlmapping/) Element angegeben, oder das [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) Element **true** ist. |
| [get_PlaceholderName](./get_placeholdername/)() override | Liest oder setzt den Namen des [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), das Platzhaltertext enthält. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_RangeEnd](./get_rangeend/)() | Gibt das Ende des Bereichs an, wenn das [StructuredDocumentTag](../structureddocumenttag/) ein Bereichs‑Strukturiertes‑Dokument‑Tag ist. Andernfalls wird **null** zurückgegeben. |
| [get_SdtType](./get_sdttype/)() override | Ruft den Typ dieses strukturierten Dokumenten‑Tags ab. |
| [get_Tag](./get_tag/)() const override | Gibt ein Tag an, das dem aktuellen Knoten des strukturierten Dokumenten‑Tags zugeordnet ist. Darf nicht **null** sein. |
| [get_Title](./get_title/)() const override | Gibt den Anzeigenamen an, der diesem strukturierten Dokumenten‑Tag zugeordnet ist. Darf nicht **null** sein. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Liest einen String, der das XML darstellt, das im Knoten im [FlatOpc](../../aspose.words/saveformat/)‑Format enthalten ist. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Liest einen String, der das im Knoten enthaltene XML im [FlatOpc](../../aspose.words/saveformat/)-Format darstellt. Im Gegensatz zur [WordOpenXML](./get_wordopenxml/)-Eigenschaft erzeugt diese Methode ein vereinfachtes Dokument, das alle nicht inhaltbezogenen Teile ausschließt. |
| [get_XmlMapping](./get_xmlmapping/)() override | Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokumenten‑Tag‑Bereichs zu XML‑Daten in einem benutzerdefinierten XML‑Teil des aktuellen Dokuments darstellt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Gibt eine Live‑Sammlung von Kindknoten zurück, die den angegebenen Typen entsprechen. |
| [GetEnumerator](./getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](./removeallchildren/)() | Entfernt alle Knoten zwischen diesem Bereich‑Startknoten und dem Bereich‑Endknoten. |
| [RemoveSelfOnly](./removeselfonly/)() override | Entfernt diesen Bereich‑Start- und die entsprechenden Bereich‑Endknoten des strukturierten Dokumenten‑Tags, lässt jedoch dessen Inhalt im Dokumentbaum erhalten. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Setter für [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Initialisiert eine neue Instanz der Klasse **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man die Eigenschaften von mehrabschnittigen strukturierten Dokument-Tags abruft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Siehe auch

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
