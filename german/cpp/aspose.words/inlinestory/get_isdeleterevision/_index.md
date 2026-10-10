---
title: "Aspose::Words::InlineStory::get_IsDeleteRevision Methode"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::InlineStory::get_IsDeleteRevision-Methode. Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung in C++ aktiviert war."
type: docs
weight: 5000
url: /de/cpp/aspose.words/inlinestory/get_isdeleterevision/
---
## InlineStory::get_IsDeleteRevision method


Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

```cpp
bool Aspose::Words::InlineStory::get_IsDeleteRevision()
```


## Beispiele



Zeigt, wie man revisionsbezogene Eigenschaften von [InlineStory](../)-Knoten anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// Wenn wir das Dokument bearbeiten, während die Option "Track Changes" aktiviert ist, zu finden über Review -> Tracking,
// ist in Microsoft Word aktiviert, zählen die von uns vorgenommenen Änderungen als Revisionen.
// Beim Bearbeiten eines Dokuments mit Aspose.Words können wir die Verfolgung von Revisionen starten, indem wir
// die Methode "StartTrackRevisions" des Dokuments aufrufen und die Verfolgung mit der Methode "StopTrackRevisions" beenden.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu übernehmen
// oder lehnen Sie sie ab, um die vorgeschlagene Änderung rückgängig zu machen und zu verwerfen.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Unten sind fünf Arten von Revisionen aufgeführt, die einen InlineStory-Knoten kennzeichnen können.
// 1 -  Eine "insert"-Revision:
// Diese Revision tritt auf, wenn wir Text einfügen, während wir Änderungen nachverfolgen.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  Eine "move from"-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// während wir Änderungen nachverfolgen, erscheinen zwei Revisionen.
// Die "move from"-Revision ist eine Kopie des Textes, wie er ursprünglich war, bevor wir ihn verschoben haben.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  Eine "move to"-Revision:
// Die "move to"-Revision ist der Text, den wir an seiner neuen Position im Dokument verschoben haben.
// "Move from"- und "move to"-Revisionen erscheinen paarweise für jede von uns durchgeführte Verschiebungsrevision.
// Das Akzeptieren einer move revision löscht die "move from"-Revision und ihren Text,
// und behält den Text der "move to"-Revision bei.
// Das Ablehnen einer move revision hingegen behält die "move from"-Revision bei und löscht die "move to"-Revision.
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  Eine "delete"-Revision:
// Diese Revision tritt auf, wenn wir Text löschen, während wir Änderungen nachverfolgen. Wenn wir Text auf diese Weise löschen,
// bleibt er im Dokument als Revision, bis wir die Revision entweder akzeptieren,
// was den Text endgültig löscht, oder die Revision ablehnen, was den gelöschten Text an seiner Stelle belässt.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## Siehe auch

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
