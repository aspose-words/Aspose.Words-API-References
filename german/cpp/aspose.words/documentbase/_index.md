---
title: "Aspose::Words::DocumentBase Klasse"
linktitle: "DocumentBase"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase Klasse. Stellt die abstrakte Basisklasse für ein Hauptdokument und ein Glossar-Dokument eines Word-Dokuments bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 21000
url: /de/cpp/aspose.words/documentbase/
---
## DocumentBase class


Stellt die abstrakte Basisklasse für ein Hauptdokument und ein Glossar-Dokument eines Word-Dokuments bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Akzeptiert einen Besucher. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Wenn in einer abgeleiteten Klasse implementiert, ruft sie die VisitXXXEnd-Methode des angegebenen Dokumentenbesuchers auf. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Wenn in einer abgeleiteten Klasse implementiert, ruft sie die VisitXXXStart-Methode des angegebenen Dokumentenbesuchers auf. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_BackgroundShape](./get_backgroundshape/)() const | Liest oder legt die Hintergrundform des Dokuments fest. Kann **null** sein. |
| [get_Count](../compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_Document](./get_document/)() const override | Liest diese Instanz. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FontInfos](./get_fontinfos/)() const | Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten. |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | Bietet Zugriff auf die im Dokument definierten Fußnoten-/Endnoten‑Trennzeichen. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_Lists](./get_lists/)() const | Stellt Zugriff auf die im Dokument verwendete Listformatierung bereit. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Ermittelt den Typ dieses Knotens. |
| [get_PageColor](./get_pagecolor/)() | Liest oder setzt die Seitenfarbe des Dokuments. Diese Eigenschaft ist eine vereinfachte Version von [BackgroundShape](./get_backgroundshape/). |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [get_Styles](./get_styles/)() const | Gibt eine Sammlung von im Dokument definierten Stilen zurück. |
| [get_WarningCallback](./get_warningcallback/)() const | Wird während verschiedener Dokumentverarbeitungsabläufe aufgerufen, wenn ein Problem erkannt wird, das zu Daten‑ oder Formatierungsverlust führen könnte. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetText](../compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Wählt den ersten [Node](../node/) aus, der dem XPath‑Ausdruck entspricht. |
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Setter für [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | Setter für [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter für [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Aspose.Words stellt ein Word-Dokument als Baum von Knoten dar. [DocumentBase](./) ist ein Wurzelknoten des Baums, der alle anderen Knoten des Dokuments enthält.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## Beispiele



Zeigt, wie die Unterklassen von [DocumentBase](./) initialisiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## Siehe auch

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
