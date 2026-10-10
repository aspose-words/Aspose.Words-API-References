---
title: "Aspose::Words::RunCollection Klasse"
linktitle: "RunCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RunCollection Klasse. Bietet typisierten Zugriff auf eine Sammlung von Run-Knoten. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 57000
url: /de/cpp/aspose.words/runcollection/
---
## RunCollection class


Bietet typisierten Zugriff auf eine Sammlung von [Run](../run/) Knoten. Um mehr zu erfahren, besuchen Sie den [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) Dokumentationsartikel.

```cpp
class RunCollection : public Aspose::Words::NodeCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get_Count](../nodecollection/get_count/)() | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft ein [Run](../run/) am angegebenen Index ab. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](./toarray/)() | Kopiert alle Runs aus der Sammlung in ein neues Array von Runs. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
