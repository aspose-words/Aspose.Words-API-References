---
title: "Aspose::Words::Comment Klasse"
linktitle: "Kommentar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment Klasse. Stellt einen Container für den Text eines Kommentars dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words/comment/
---
## Comment class


Stellt einen Container für den Text eines Kommentars dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende des Kommentars zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Anfang des Kommentars zu besuchen. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Fügt diesem Kommentar eine Antwort hinzu. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialisiert eine neue Instanz der [Comment](./) Klasse. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Initialisiert eine neue Instanz der [Comment](./) Klasse. |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Wenn das letzte Kind kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [get_Ancestor](./get_ancestor/)() | Gibt das übergeordnete [Comment](./) Objekt zurück. Gibt **null** für Kommentare auf oberster Ebene zurück. |
| [get_Author](./get_author/)() const | Gibt den Autorennamen eines Kommentars zurück oder setzt ihn. |
| [get_Count](../compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_DateTime](./get_datetime/)() const | Ermittelt Datum und Uhrzeit, zu der der Kommentar erstellt wurde. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Ermittelt das UTC-Datum und die UTC-Uhrzeit, zu der der Kommentar erstellt wurde. |
| virtual [get_Document](../node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_Done](./get_done/)() const | Ermittelt oder setzt das Flag, das anzeigt, dass der Kommentar als erledigt markiert wurde. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Ermittelt den ersten Absatz in der Geschichte. |
| [get_Font](../inlinestory/get_font/)() | Bietet Zugriff auf die Schriftformatierung des Ankerzeichens dieses Objekts. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_Id](./get_id/)() const | Liest oder setzt die Kommentar-ID. |
| [get_Initial](./get_initial/)() const | Liefert oder setzt die Initialen des Benutzers, der mit einem bestimmten Kommentar verknüpft ist. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Ermittelt den letzten Absatz in der Geschichte. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Liefert [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Ermittelt eine Sammlung von Absätzen, die direkte Kindknoten der Geschichte sind. |
| [get_ParentId](./get_parentid/)() const | Liest die übergeordnete Kommentar-ID. Ein Wert von **%-1** bedeutet, dass der Kommentar keinen Elternteil hat. |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Ruft das übergeordnete [Paragraph](../paragraph/) dieses Knotens ab. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_Replies](./get_replies/)() | Liefert eine Sammlung von [Comment](./)-Objekten, die unmittelbare Kinder des angegebenen Kommentars sind. |
| [get_StoryType](./get_storytype/)() override | Liefert [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Ermittelt eine Sammlung von Tabellen, die direkte Kindknoten der Geschichte sind. |
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
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveAllReplies](./removeallreplies/)() | Entfernt alle Antworten auf diesen Kommentar. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Entfernt die angegebene Antwort auf diesen Kommentar. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Wählt den ersten [Node](../node/) aus, der dem XPath‑Ausdruck entspricht. |
| [set_Author](./set_author/)(const System::String\&) | Setter für [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Ermittelt Datum und Uhrzeit, zu der der Kommentar erstellt wurde. |
| [set_Done](./set_done/)(bool) | Setter für [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Setter für [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Setter für [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Setzt die übergeordnete Kommentar-ID. Ein Wert von **%-1** bedeutet, dass der Kommentar keinen Elternteil hat. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Dies ist eine Komfortmethode, die das einfache Festlegen des Textes des Kommentars ermöglicht. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Ein Kommentar ist eine Anmerkung, die an einem Textbereich oder an einer Position im Text verankert ist. Ein Kommentar kann eine beliebige Menge an Block‑Inhalt enthalten.

Wenn ein [Comment](./)-Objekt allein vorkommt, ist der Kommentar an der Position des [Comment](./)-Objekts verankert.

Um einen Kommentar an einem Textbereich zu verankern, sind drei Objekte erforderlich: [Comment](./), [CommentRangeStart](../commentrangestart/) und [CommentRangeEnd](../commentrangeend/). Alle drei Objekte müssen denselben [Id](./get_id/)-Wert teilen.

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Beispiele



Zeigt, wie man einem Dokument einen Kommentar hinzufügt und darauf antwortet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Platziere den Kommentar an einem Knoten im Dokumentenkörper.
// Dieser Kommentar wird an der Position seines Absatzes angezeigt,
// außerhalb des rechten Seitenrandes und mit einer gepunkteten Linie, die ihn mit seinem Absatz verbindet.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Füge eine Antwort hinzu, die unter dem übergeordneten Kommentar angezeigt wird.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Kommentare und Antworten sind beide Comment‑Knoten.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Kommentare, die nicht auf andere Kommentare antworten, sind "Top‑Level". Sie haben keine übergeordneten Kommentare.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Antworten haben einen übergeordneten Top‑Level‑Kommentar.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


Zeigt, wie man einem Absatz einen Kommentar hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word können wir diesen Kommentar im Dokumentenkörper rechtsklicken, um ihn zu bearbeiten oder darauf zu antworten.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Siehe auch

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
