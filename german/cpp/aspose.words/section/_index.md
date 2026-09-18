---
title: "Aspose::Words::Section Klasse"
linktitle: "Abschnitt"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section Klasse. Stellt einen einzelnen Abschnitt in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 58000
url: /de/cpp/aspose.words/section/
---
## Section class


Stellt einen einzelnen Abschnitt in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class Section : public Aspose::Words::CompositeNode,
                public Aspose::Words::ISectionAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Wenn in einer abgeleiteten Klasse implementiert, ruft sie die VisitXXXEnd-Methode des angegebenen Dokumentenbesuchers auf. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Wenn in einer abgeleiteten Klasse implementiert, ruft sie die VisitXXXStart-Methode des angegebenen Dokumentenbesuchers auf. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendContent](./appendcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | Fügt eine Kopie des Inhalts des Quellabschnitts am Ende dieses Abschnitts ein. |
| [ClearContent](./clearcontent/)() | Löscht den Abschnitt. |
| [ClearHeadersFooters](./clearheadersfooters/)() | Löscht die Kopf- und Fußzeilen dieses Abschnitts. |
| [ClearHeadersFooters](./clearheadersfooters/)(bool) | Löscht die Kopf- und Fußzeilen dieses Abschnitts. |
| [Clone](./clone/)() | Erstellt ein Duplikat dieses Abschnitts. |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [DeleteHeaderFooterShapes](./deleteheaderfootershapes/)() | Löscht alle Formen (Zeichnungsobjekte) aus den Kopf- und Fußzeilen dieses Abschnitts. |
| [EnsureMinimum](./ensureminimum/)() | Stellt sicher, dass der Abschnitt ein [Body](./get_body/) mit einem [Paragraph](../paragraph/) hat. |
| [get_Body](./get_body/)() | Gibt den untergeordneten Knoten [Body](../body/) des Abschnitts zurück. |
| [get_Count](../compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](../node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_HeadersFooters](./get_headersfooters/)() | Bietet Zugriff auf die Knoten der Kopf- und Fußzeilen des Abschnitts. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [Section](../nodetype/) zurück. |
| [get_PageSetup](./get_pagesetup/)() | Gibt ein Objekt zurück, das die Seiteneinrichtung und Abschnittseigenschaften darstellt. |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectedForForms](./get_protectedforforms/)() | True, wenn der Abschnitt für Formulare geschützt ist. Wenn ein Abschnitt für Formulare geschützt ist, können Benutzer in Microsoft Word nur Text in Formularfeldern auswählen und ändern. |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetText](../compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PrependContent](./prependcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | Fügt eine Kopie des Inhalts des Quellabschnitts am Anfang dieses Abschnitts ein. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [Section](./section/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialisiert eine neue Instanz der [Section](./) Klasse. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Wählt den ersten [Node](../node/) aus, der dem XPath‑Ausdruck entspricht. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ProtectedForForms](./set_protectedforforms/)(bool) | Setter für [Aspose::Words::Section::get_ProtectedForForms](./get_protectedforforms/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


[Section](./) can have one [Body](../body/) and maximum one [HeaderFooter](../headerfooter/) of each [HeaderFooterType](../headerfootertype/). [Body](../body/) and [HeaderFooter](../headerfooter/) nodes can be in any order inside [Section](./).

Ein minimal gültiger Abschnitt muss ein [Body](../body/) mit einem [Paragraph](../paragraph/) besitzen.

Jeder Abschnitt hat seine eigenen Eigenschaften, die Seitengröße, Orientierung, Ränder usw. festlegen.

Sie können eine Kopie eines Abschnitts mit [Clone()](../node/clone/) erstellen. Die Kopie kann in dasselbe oder ein anderes Dokument eingefügt werden.

Um einen gesamten Abschnitt einschließlich Abschnittsumbruch und Abschnittseigenschaften hinzuzufügen, einzufügen oder zu entfernen, verwenden Sie die Methoden des [Sections](../document/get_sections/) Objekts.

Um nur den Inhalt des Abschnitts ohne den Abschnittsumbruch und die Abschnittseigenschaften zu kopieren und einzufügen, verwenden Sie die Methoden [AppendContent()](../) und [PrependContent()](../).

## Beispiele



Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und erhalten ein Dokumentenknoten ohne Kinder.
doc->RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
// Erstellen Sie zunächst einen neuen Abschnitt und fügen Sie ihn dann als Kind zum Wurzel-Dokumentenknoten hinzu.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt.
// auf der Seite zwischen der Kopf‑ und Fußzeile des Abschnitts.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Fügen Sie schließlich etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
// setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Siehe auch

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
