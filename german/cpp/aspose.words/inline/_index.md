---
title: "Aspose::Words::Inline Klasse"
linktitle: "Inline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Inline Klasse. Basisklasse für Inline‑Ebene‑Knoten, die Zeichenformatierungen zugeordnet bekommen können, aber keine eigenen Kindknoten haben dürfen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 36000
url: /de/cpp/aspose.words/inline/
---
## Inline class


Basisklasse für Inline‑Ebene‑Knoten, die eine Zeichenformatierung besitzen können, aber keine eigenen Kindknoten haben dürfen. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Akzeptiert einen Besucher. |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](../node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_Font](./get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Liefert **true**, wenn dieser Knoten andere Knoten enthalten kann. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Ermittelt den Typ dieses Knotens. |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](./get_parentparagraph/)() | Ruft das übergeordnete [Paragraph](../paragraph/) dieses Knotens ab. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Eine von [Inline](./) abgeleitete Klasse kann ein Kind von [Paragraph](../paragraph/) sein.

## Beispiele



Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Wenn wir das Dokument bearbeiten, während die Option "Track Changes" aktiviert ist, zu finden über Review -> Tracking,
// ist in Microsoft Word aktiviert, zählen die von uns vorgenommenen Änderungen als Revisionen.
// Beim Bearbeiten eines Dokuments mit Aspose.Words können wir die Verfolgung von Revisionen starten, indem wir
// die Methode "StartTrackRevisions" des Dokuments aufrufen und die Verfolgung mit der Methode "StopTrackRevisions" beenden.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu übernehmen
// oder sie ablehnen, um die vorgeschlagene Änderung effektiv zu ändern.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Der übergeordnete Knoten einer Revision ist der Run, den die Revision betrifft. Ein Run ist ein Inline-Knoten.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Unten sind fünf Arten von Revisionen aufgeführt, die einen Inline-Knoten markieren können.
// 1 -  Eine "insert"-Revision:
// Diese Revision tritt auf, wenn wir Text einfügen, während wir Änderungen nachverfolgen.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Eine "format"-Revision:
// Diese Revision tritt auf, wenn wir die Formatierung von Text ändern, während wir Änderungen nachverfolgen.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Eine "move from"-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// während wir Änderungen nachverfolgen, erscheinen zwei Revisionen.
// Die "move from"-Revision ist eine Kopie des Textes, wie er ursprünglich war, bevor wir ihn verschoben haben.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Eine "move to"-Revision:
// Die "move to"-Revision ist der Text, den wir an seiner neuen Position im Dokument verschoben haben.
// "Move from"- und "move to"-Revisionen erscheinen paarweise für jede von uns durchgeführte Verschiebungsrevision.
// Das Akzeptieren einer move revision löscht die "move from"-Revision und ihren Text,
// und behält den Text der "move to"-Revision bei.
// Das Ablehnen einer move revision hingegen behält die "move from"-Revision bei und löscht die "move to"-Revision.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Eine "delete"-Revision:
// Diese Revision tritt auf, wenn wir Text löschen, während wir Änderungen nachverfolgen. Wenn wir Text auf diese Weise löschen,
// bleibt er im Dokument als Revision, bis wir die Revision entweder akzeptieren,
// was den Text endgültig löscht, oder die Revision ablehnen, was den gelöschten Text an seiner Stelle belässt.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Siehe auch

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
