---
title: "Aspose::Words::RevisionType Enum"
linktitle: "RevisionType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionType Enum. Gibt den Typ der Änderung an, die in Revision in C++ verfolgt wird."
type: docs
weight: 113000
url: /de/cpp/aspose.words/revisiontype/
---
## RevisionType enum


Gibt den Typ der Änderung an, die in [Revision](../revision/) verfolgt wird.

```cpp
enum class RevisionType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Einfügung | 0 | Neuer Inhalt wurde im Dokument eingefügt. |
| Löschung | 1 | Inhalt wurde aus dem Dokument entfernt. |
| Formatänderung | 2 | Eine Formatänderung wurde auf den übergeordneten Knoten angewendet. |
| Stildefinitionsänderung | 3 | Eine Formatänderung wurde auf den übergeordneten Stil angewendet. |
| Verschieben | 4 | Inhalt wurde im Dokument verschoben. |


## Beispiele



Zeigt, wie man mit Revisionen in einem Dokument arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normales Bearbeiten des Dokuments wird nicht als Revision gezählt.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// Um unsere Änderungen als Revisionen zu registrieren, müssen wir einen Autor deklarieren und dann beginnen, sie zu verfolgen.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Dieses Flag entspricht der Option "Review" -> "Tracking" -> "Track Changes" in Microsoft Word.
// Die Methode "StartTrackRevisions" beeinflusst ihren Wert nicht,
// und das Dokument verfolgt Revisionen programmatisch, obwohl es den Wert "false" hat.
// Wenn wir dieses Dokument mit Microsoft Word öffnen, wird es keine Revisionen verfolgen.
ASSERT_FALSE(doc->get_TrackRevisions());

// Wir haben Text mit dem Document Builder hinzugefügt, sodass die erste Revision eine Einfüge‑Revision ist.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Entfernen Sie einen Run, um eine Lösch‑Revision zu erstellen.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Das Hinzufügen einer neuen Revision platziert sie am Anfang der Revisionssammlung.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Einfüge‑Revisionen erscheinen im Dokumentkörper, noch bevor wir die Revision akzeptieren/ablehnen.
// Das Ablehnen der Revision entfernt ihre Knoten aus dem Dokumentkörper. Umgekehrt bleiben Knoten, die Lösch‑Revisionen bilden
// auch im Dokument, bis wir die Revision akzeptieren.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Das Akzeptieren der Lösch‑Revision entfernt ihren übergeordneten Knoten aus dem Absatztext
// und anschließend die Revision der Sammlung selbst entfernen.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Verschieben Sie jetzt den Knoten, um einen bewegten Revisionstyp zu erstellen.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// Die verschobene Revision befindet sich jetzt bei Index 1. Verwerfen Sie die Revision, um ihren Inhalt zu verwerfen.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
