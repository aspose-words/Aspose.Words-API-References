---
title: "Aspose::Words::Document::StartTrackRevisions Methode"
linktitle: "StartTrackRevisions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::StartTrackRevisions Methode. Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen in C++ zu markieren."
type: docs
weight: 92000
url: /de/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
## Hinweise


Wenn Sie diese Methode aufrufen und anschließend einige Änderungen programmgesteuert am Dokument vornehmen, das Dokument speichern und später in MS Word öffnen, werden Sie diese Änderungen als Revisionen sehen.

Derzeit unterstützt Aspose.Words nur das Verfolgen von Knoten‑einfügungen und -löschungen. Formatierungsänderungen werden nicht als Revisionen erfasst.

Automatisches Verfolgen von Änderungen wird sowohl beim Ändern dieses Dokuments durch Knotenmanipulationen als auch bei der Verwendung von [DocumentBuilder](../../documentbuilder/) unterstützt.

Diese Methode ändert die Option [TrackRevisions](../get_trackrevisions/) nicht und verwendet ihren Wert nicht für das Verfolgen von Revisionen.

## Beispiele



Zeigt, wie man Revisionen beim Bearbeiten eines Dokuments verfolgt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Das Bearbeiten eines Dokuments wird normalerweise nicht als Revision gezählt, bis wir mit der Verfolgung beginnen.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Stoppen Sie die Verfolgung von Revisionen, damit zukünftige Änderungen nicht als Revisionen gezählt werden.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Das Erstellen von Revisionen gibt ihnen ein Datum und eine Uhrzeit der Operation.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir die Verfolgung von Revisionen starten.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Wir können diese Revisionen programmgesteuert akzeptieren/ablehnen
// indem wir Methoden wie Document.AcceptAllRevisions oder die Accept-Methode jeder einzelnen Revision aufrufen.
// In Microsoft Word können wir sie manuell über \"Review\" -> \"Changes\" verarbeiten.
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Autor | const System::String\& | Initialen des Autors, die für Revisionen verwendet werden. |
| dateTime | System::DateTime | Das Datum und die Uhrzeit, die für Revisionen verwendet werden sollen. |
## Hinweise


Wenn Sie diese Methode aufrufen und anschließend einige Änderungen programmgesteuert am Dokument vornehmen, das Dokument speichern und später in MS Word öffnen, werden Sie diese Änderungen als Revisionen sehen.

Derzeit unterstützt Aspose.Words nur das Verfolgen von Knoten‑einfügungen und -löschungen. Formatierungsänderungen werden nicht als Revisionen erfasst.

Automatisches Verfolgen von Änderungen wird sowohl beim Ändern dieses Dokuments durch Knotenmanipulationen als auch bei der Verwendung von [DocumentBuilder](../../documentbuilder/) unterstützt.

Diese Methode ändert die Option [TrackRevisions](../get_trackrevisions/) nicht und verwendet ihren Wert nicht für das Verfolgen von Revisionen.

## Beispiele



Zeigt, wie man Revisionen beim Bearbeiten eines Dokuments verfolgt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Das Bearbeiten eines Dokuments wird normalerweise nicht als Revision gezählt, bis wir mit der Verfolgung beginnen.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Stoppen Sie die Verfolgung von Revisionen, damit zukünftige Änderungen nicht als Revisionen gezählt werden.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Das Erstellen von Revisionen gibt ihnen ein Datum und eine Uhrzeit der Operation.
// Wir können dies deaktivieren, indem wir DateTime.MinValue übergeben, wenn wir die Verfolgung von Revisionen starten.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Wir können diese Revisionen programmgesteuert akzeptieren/ablehnen
// indem wir Methoden wie Document.AcceptAllRevisions oder die Accept-Methode jeder einzelnen Revision aufrufen.
// In Microsoft Word können wir sie manuell über \"Review\" -> \"Changes\" verarbeiten.
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
